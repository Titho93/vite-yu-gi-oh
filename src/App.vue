<script>

import axios from 'axios'
import { store } from './data/store';
import Main from './components/Main.vue';

export default {
  name: 'App',
  components: {
    Main
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

  <h1>Yu-Gi-Oh</h1>
  <Main />
  
</template>

<style lang="scss">

@use './scss/Main.scss';

</style>