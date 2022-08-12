<script>
export default {
  data() {
    return {
    }
  }
}
</script>

<template>
  <div class="pokemon-cards__card">
    <img src="https://img.pokemondb.net/sprites/x-y/normal/bulbasaur.png" alt="A pokemon">
    <div class="pokemon-cards__card--info">
      <h2 id="pokemon-name">Name</h2>
      <span id="pokemon-info">Information</span>
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
    left: -20px;
    top: -30px;
  }

  .pokemon-cards__card--info {
    padding-left: 80px;
  }

  .pokemon-cards__card--info > h2 {
    font-size: medium;
    font-weight: bold;
  }
</style>