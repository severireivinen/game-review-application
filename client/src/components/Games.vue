<template>
  
  <div class="grid-container">
    <div class="grid-item" :key="game.id" v-for="game in games">
      <Game :game="game" />
    </div>
  </div>
</template>

<script>
import Game from "./Game";

export default {
  name: "Games",
  props: {
    games: Array,
  },
  components: {
    Game,
  },
};
</script>

<style>
.grid-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(325px, 1fr));
}
</style>
