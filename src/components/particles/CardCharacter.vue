<template>
  <div class="container center">
    <img :src="character.image">
    <h3>{{character.name}}</h3>
    <hr>
    <div>{{character.location.name}}</div>
    <p>{{character.species}}</p>
  </div>
</template>

<script>
export default {
  name: 'CardCharacter',
  props: {
    character: Object,
  }
}
</script>

<style lang='scss' scoped>
  img {
    max-width: 100%;
    border-radius: 50%;
    box-shadow: 5px 5px 7px #5c5b5b;
    margin: 10px;
  }
  hr {
    opacity: 1;
  }

  h3 {
    margin: 20px;
  }
  p {
    margin: 10px;
    font-weight: bold;
  }

  .center {
    text-align: center;
  }
</style>