<script>

import { store } from '../../data/store'

export default {
    name: 'SelectBar',
    data() {
        return{
            store
        }
    }
}
</script>

<template>
  
    <select v-model="store.searchArchetype" name="type" id="">
        <option value="">All</option>
        <option value="Alien">Alien</option>
        <option value="Noble Knight">Noble Knight</option>
        <option value="Sinful Spoils">Sinful Spoils</option>
    </select>
    <button @click="$emit('startSearch')">Search</button>


</template>

<style lang="scss" scoped>

select {
  background-color: white;
  border-radius: 5px;
  width: 120px;
  padding: 5px 10px;
  margin: 20px 10px;
  border: none;
}

</style>