<template>
  <div>
    <router-link to="/game">
      <button
        @click="restart()"
        class="wording nes-btn is-primary"
      >Challenge</button>
    </router-link>
    <router-link to="/practice">
      <button
        @click="restart()"
        class="wording nes-btn is-success"
      >Practice</button>
    </router-link>
  </div>
</template>

<script>
import { mapActions } from 'vuex';

export default {
  // Component name
  name: 'SelectGameType',
  methods: {
    ...mapActions(['guessFlag', 'setGameMode', 'getRandomFlag', 'getRandomOptions', 'setScoreInitial']),
    restart () {
      this.setScoreInitial();
      // Set the game mode
      this.setGameMode('challenge');
      // Get a random flag
      this.getRandomFlag();
      // Get options
      this.getRandomOptions();
    }
  }
};
</script>

<style lang="scss" scoped>
div {
  margin: 1.5rem;
}
.wording {
  font-size: .9rem;
  border-radius: 5px;
  color: white !important;
  font-weight: bolder;
  padding: 0 16px;
  height: 56px;
  margin-right: 16px;
}
</style>
