<script setup>
  import PokemonCard from '@/components/PokemonCard.vue'
</script>

<template>
  <div class="pokemon-selector">
    <img class="pokemon-selector__main-image" src="@/assets/pokemon-bg.jpg" alt="A picture of a pokemon">

    <div class="pokemon-selector__type">
      <label for="type-select" class="pokemon-selector__type--label">Select type:</label>
      <select name="type-select" class="pokemon-selector__type--select">
        <option default value="Grass">Grass</option>
      </select>
    </div>
    
    <div class="pokemon-selector__cards">
      <PokemonCard v-for="index in 10" :key="index"/>
    </div>
    <div class="pokemon-selector__button">
      <button>Load</button>
    </div>
  </div>
</template>

<script>
export default {
  components: {
    PokemonCard,
  },
  data() {
    return {
    }
  }
}
</script>

<style scoped>
  .pokemon-selector__container {
    width: 100%;
  }

  .pokemon-selector__main-image {
    width: 100%;
    padding: 0 10px;
  }

  .pokemon-selector__type {
    width: 80%;
    margin: 0 auto;
    padding: 10px;
    position: relative;
  }

  .pokemon-selector__type--select {
    width: 100%;
    padding: 10px;
    border: 1px solid black;
  }

  .pokemon-selector__cards {
    margin-top: 20px;
    height: 400px;
    overflow-y: scroll;
    border-bottom: 1px solid gray;
    padding: 0 10px;
  }

  .pokemon-selector__button {
    display: flex;
    justify-content: space-around;
    width: 100%;
    margin: 20px 10px;
    height: 40px;
    text-align: center
  }

  .pokemon-selector__button > button {
    width: 100%;
    font-size: large;
    background: #3942A9;
    border: none;
    color: white;
    text-transform: uppercase;
  }
</style>