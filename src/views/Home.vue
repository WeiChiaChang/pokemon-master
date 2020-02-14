<template>
  <div class="container">
    <img src="../assets/loading.gif" alt="TW Icon Game" />
    <h2 class="md-display-6">Pokemon Master</h2>
    <select-game-type />
    <select-language />
  </div>
</template>

<script>
import SelectGameType from '@/components/SelectGameType.vue';
import SelectLanguage from '@/components/SelectLanguage.vue';

export default {
  name: 'App',
  components: {
    SelectGameType,
    SelectLanguage
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
