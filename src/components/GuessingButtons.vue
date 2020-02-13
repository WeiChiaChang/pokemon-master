<template>
  <md-content>
    <md-button
      v-for="flag in flags"
      v-bind:key="`guessbutton-${flag.code}`"
      @click="onClick(flag.code)"
      :disabled="justGuessed"
      class="btn_wording"
      v-bind:class="{
        'correct': justGuessed && correctFlag.code === flag.code,
        'wrong': justGuessed && currentGuess === flag.code && correctFlag.code !== flag.code,
      }"
    >{{flag[currentLanguage]}}</md-button>
  </md-content>
</template>

<script>
import { mapState } from 'vuex';

export default {
  // Component name
  name: 'GuessingButtons',

  // Imported components
  props: {
    flags: Array,
    justGuessed: Boolean,
    currentGuess: String,
    correctFlag: Object,
  },

  // Methods
  methods: {
    onClick(code) {
      this.$emit('guess', code);
    },
  },
  computed: {
    ...mapState({
      currentLanguage: ({ currentLanguage }) => currentLanguage,
    }),
  },
};
</script>

<style lang="scss" scoped>
.md-button {
  display: block;
  width: 100%;
  height: 50px;
  margin: 0;
  margin-bottom: 10px;
  border: 2px solid #3e3e3e;
  text-transform: capitalize;
}
.correct {
  background-color: #239e23 !important;
  color: white !important;
}
.wrong {
  background-color: #c21a1a !important;
  color: white !important;
}
.buttons-container {
  background: transparent !important;
}
.btn_wording {
  font-size: 1rem;
  background: wheat;
}
</style>
