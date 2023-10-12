<script>

import axios from 'axios'
import { store } from './data/store';
import Header from './components/Header.vue';
import CardsContainer from './components/CardsContainer.vue'

export default {
  name: 'App',
  components: {
    Header,
    CardsContainer
  },
  data(){
    return{
      store
    }
  },
  methods: {
    getApi(){
      axios.get(store.apiUrl)
        .then( res => {
          console.log(res.data);
          store.cardsList = res.data.results;
        })
        .catch(err => {
          console.log(err);
        })
    }
  },
  mounted(){
    this.getApi()
  }
}
</script>

<template>

  <Header />
  <Main>
    <CardsContainer />

  </Main>
  
  
</template>

<style lang="scss">

@use './scss/Main.scss';

</style>