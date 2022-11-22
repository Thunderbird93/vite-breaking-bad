<script>
export default {
  name: 'CharacterCard',
  data(){
    return{
    }
  },
  props:{
    character: Object
  }
}
</script>

<template>
  <div class="carta">
    <div class="picture">
        <img :src=character.img :alt="character.name">
    </div>
    <div class="info">
        <h3>{{character.name}}</h3>
        <h5>{{character.category}}</h5>
        <h6>{{character.status}}</h6>
    </div>
  </div>
</template>

<style lang="scss" scoped>

img {
    width: 100%;
}

.carta{
    border: 1px dotted black;
    max-width: calc(100%/5);
    display: flex;
    flex-direction: column;
    margin: 5px;
    padding: 5px;
}
</style>