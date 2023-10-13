<script>

import axios from 'axios'
import { store } from './data/store';
import Header from './components/Header.vue';
import CardsContainer from './components/CardsContainer.vue'
import Result from './components/partials/Result.vue'
import SelectBar from './components/partials/SelectBar.vue'

export default {
  name: 'App',
  components: {
    Header,
    CardsContainer,
    Result,
    SelectBar
  },
  data(){
    return{
      store
    }
  },
  methods: {
    getApi(){
      axios.get(store.apiUrl, {
        params:{
          archetype: store.searchArchetype
        }
      })
        .then( res => {
          console.log(res.data);
          store.cardsList = res.data.data;
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
  <main>
    <div class="container">
      <SelectBar @startSearch="getApi" />
      <div class="container b">
        <Result/>
        <CardsContainer />
      </div>

    </div>

  </main>
  
  
</template>

<style lang="scss">

@use './scss/Main.scss';

.container.b {
    background-color: white;
    height: 100%;
}
</style>