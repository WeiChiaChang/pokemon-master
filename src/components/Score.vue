<template>
  <md-table>
    <md-table-row>
      <md-table-head md-numeric>Now</md-table-head>
    </md-table-row>
    <md-table-row>
      <md-table-head md-numeric>{{score.total}}</md-table-head>
    </md-table-row>
  </md-table>
</template>

<script>
import { mapState } from 'vuex';

export default {
  name: 'Score',
  computed: {
    ratio() {
      if (this.score.total > 0) {
        return (100 * this.score.success / this.score.total).toFixed(2);
      }
      return '0.00';
    },
    ...mapState({
      score: ({ score }) => score,
    }),
  },
};
</script>

<style lang="scss">
.md-table-head-container {
  text-align: center;
  height: auto;
  padding: 0;
}
.md-table-head-label {
  height: 32px !important;
  line-height: 32px !important;
  padding-left: 10px !important;
  padding-right: 10px !important;
}
.md-table-head {
  font-size: 1rem;
}
.md-table-content {
  background: transparent !important;
}
</style>
