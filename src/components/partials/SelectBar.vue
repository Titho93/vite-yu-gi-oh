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
    <select v-model="store.searchArchetype" name="type" id="type">
        <option value="">Select A Card Type</option>
        <option value="Alien">Alien</option>
        <option value="Noble Knight">Noble Knight</option>
        <option value="Sinful Spoils">Sinful Spoils</option>
        <option value="-Eyes Dragon">Eyes Dragon</option>
        <option value="@Ignister">Ignister</option>
        <option value="A.I.">A.I.</option>
        <option value="ABC">ABC</option>
        <option value="Abyss Actor">Abyss Actor</option>
        <option value="Adamancipator">Adamancipator</option>
        <option value="Advanced Crystal Beast">Advanced Crystal Beast</option>
        <option value="Adventurer Token">Adventurer Token</option>
        <option value="Aesir">Aesir</option>
    </select>
    <button @click="$emit('startSearch')">Search</button>


</template>

<style lang="scss" scoped>

select {
  background-color: white;
  border-radius: 5px;
  width: 200px;
  padding: 5px 10px;
  margin: 20px 10px;
  border: none;
}

button {
    background-color: rgb(243, 9, 9);
    border-radius: 5px;
    border: 1px solid black;
}

</style>