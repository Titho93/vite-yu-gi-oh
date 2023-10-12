<script>

export default {
    name: 'CharacterCard',
    props:{
        name: String,
        archetype: String,
        image_url: String
    }
}
</script>

<template>
  
  <div class="col-2">
    <div class="bt-card">
       <img :src="image_url" alt="Card">
       <h6>{{ name }}</h6>
       <p>{{ archetype }}</p>
    </div>
  </div>

</template>

<style lang="scss">

.bt-card {
    text-align: center;
   img {
    width: 100%;
   }
   h6 {
    text-transform: uppercase;
    color: white;
    padding: 10px 0;
   }
   p {
    font-size: 16px;
    padding-bottom: 10px;
   }
}

</style>