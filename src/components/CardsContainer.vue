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

    
        <div class="row">
            <CharacterCard v-for="card in store.cardsList"
            :key="card.id"
            :name="card.name"
            :type="card.type"
            :image="card.card_images[0].image_url"
            />
        </div>
    
  
</template>

<style lang="scss" scoped>

.row{
        height: 100%;
        padding: 0px 20px;
        overflow: auto;
    }

</style>