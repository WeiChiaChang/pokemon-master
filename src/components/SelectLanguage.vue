<template>
  <div>
    <button
      @click="language('en')"
      class="nes-btn"
      v-bind:class="{ 'is-warning': currentLanguage == 'en' }"
    >en</button>
    <button @click="language('de')"
      class="nes-btn"
      v-bind:class="{ 'is-warning': currentLanguage == 'de' }"
    >de</button>
    <button @click="language('fr')"
      class="nes-btn"
      v-bind:class="{ 'is-warning': currentLanguage == 'fr' }"
    >fr</button>
    <button @click="language('ja')"
      class="nes-btn"
      v-bind:class="{ 'is-warning': currentLanguage == 'ja' }"
    >ja</button>
    <button @click="language('ko')"
      class="nes-btn"
      v-bind:class="{ 'is-warning': currentLanguage == 'ko' }"
    >ko</button>
    <button @click="language('zh')"
      class="nes-btn"
      v-bind:class="{ 'is-warning': currentLanguage == 'zh' }"
    >zh</button>
  </div>
</template>


<script>
import { mapActions, mapState } from 'vuex';

export default {
  // Component name
  name: 'SelectLanguage',
  methods: {
    ...mapActions(['setLanguage']),
    language: function(language) {
      // set the language
      this.setLanguage(language);
    },
  },
  computed: {
    ...mapState({
      currentLanguage: ({ currentLanguage }) => currentLanguage,
    }),
  },
};
</script>
