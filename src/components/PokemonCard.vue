<script>
export default {
  props:{
    pokemon: Object,
    },
  data() {
    return {
      selected: false,
    }
  },
}
</script>

<template>
  <div class="pokemon-cards__card">
    <img v-bind:src="pokemon.image" alt="A pokemon">
    <div class="pokemon-cards__card--info">
      <h2 id="pokemon-name">{{pokemon.name}}</h2>
      <span id="pokemon-info">{{pokemon.classfication}}</span>
    </div>
  </div>
</template>

<style scoped>
  .pokemon-cards__card {
    display: flex;
    height: 60px;
    padding: 5px;
    border: 1px solid black;
    margin: 20px 0;
  }

  .pokemon-cards__card > img {
    position: absolute;
    z-index: 1;
    left: 0px;
    top: 0px;
    height: 60px;
  }

  .pokemon-cards__card--info {
    padding-left: 80px;
  }

  .pokemon-cards__card--info > h2 {
    font-size: medium;
    font-weight: bold;
  }

  .selected {
    border: 2px blue solid;
    background: lightgray;
  }
</style>