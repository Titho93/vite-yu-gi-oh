<script>

import { store } from '../data/store'
import CharacterCard from './partials/CharacterCard.vue'

export default {
    name: 'CardsContainer',
    components: {
        CharacterCard
    },
    data(){
        return{
            store
        }
    },
    mounted(){
        console.log(store.cardsList);
    }
}
</script>

<template>

    <div class="container ">
        <div class="row">
            <CharacterCard v-for="card in store.cardsList"
            :key="card.id"
            :name="card.name"
            :archetype="card.type"
            :image_url="card.image_url"
            />
        </div>
    
    </div>
  
</template>

<style lang="scss" scoped>

.container {
    background-color: white;
    height: 100vh;
    .row{
        padding: 40px 20px;
    }
}


</style>