<script>

import axios from 'axios'
import { store } from './data/store';
import Header from './components/Header.vue';
import CardsContainer from './components/CardsContainer.vue'
import Result from './components/partials/Result.vue'

export default {
  name: 'App',
  components: {
    Header,
    CardsContainer,
    Result
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
      <select name="type" id="">
        <option value="All">All</option>
        <option value="Alien">Alien</option>
        <option value="Noble Knight">Noble Knight</option>
        <option value="Sinful Spoils">Sinful Spoils</option>
      </select>
      <div class="container b">
        <Result/>
        <CardsContainer />
      </div>

    </div>

  </main>
  
  
</template>

<style lang="scss">

@use './scss/Main.scss';

select {
  background-color: white;
  border-radius: 5px;
  width: 120px;
  padding: 5px 10px;
  margin: 20px 10px;
  border: none;
}

.container.b {
    background-color: white;
    height: 100%;
}
</style>