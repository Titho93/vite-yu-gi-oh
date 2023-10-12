<script>

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
  }
}
</script>

<template>
  
  <h1>{{store.titleApp}}</h1>
  <Main />
  
</template>

<style lang="scss">

@use './scss/Main.scss';

</style>