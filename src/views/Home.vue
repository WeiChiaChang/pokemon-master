<template>
  <div class="container">
    <img src="../assets/loading.gif" alt="TW Icon Game" />
    <h2 class="md-display-6">Pokemon Master</h2>
    <select-game-type />
  </div>
</template>

<script>
import SelectGameType from '@/components/SelectGameType.vue';

export default {
  name: 'App',
  components: {
    SelectGameType,
  },
};
</script>

<style scoped>
.container {
  text-align: center;
  background: transparent;
}
img {
  display: inline-block;
  margin: 3.2rem 0;
  max-width: 72%;
}
</style>
