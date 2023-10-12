<script>

export default {
    name: 'CharacterCard'
}
</script>

<template>
  
  <div class="col-2">
    <div class="bt-card">
       <img src="https://images.ygoprodeck.com/images/cards/34541863.jpg" alt="Card">
       <h6>Name card</h6>
       <p>Species</p>
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