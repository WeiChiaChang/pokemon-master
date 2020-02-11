<template>
  <div class="container">
    <img src="../assets/loading.gif" alt="TW Icon Game" />
    <h1 class="md-display-6">Pokemon Master</h1>
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
  margin-bottom: 3.2rem;
  max-width: 72%;
}
</style>
