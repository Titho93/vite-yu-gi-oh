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

    <div>
        <CharacterCard />
    </div>
  
</template>

<style lang="scss" scoped>

</style>