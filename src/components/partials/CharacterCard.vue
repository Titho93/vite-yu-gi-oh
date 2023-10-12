<script>

export default {
    name: 'CharacterCard',
    props:{
        name: String,
        type: String,
        image: String
    }
}
</script>

<template>
  
  <div class="col-2">
    <div class="bt-card">
       <img :src="image" alt="Card">
       <h6>{{ name }}</h6>
       <p>{{ type }}</p>
    </div>
  </div>

</template>

<style lang="scss">

.col-2 {
    display: flex;
    align-items: stretch;
    margin-bottom: 20px;
}

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