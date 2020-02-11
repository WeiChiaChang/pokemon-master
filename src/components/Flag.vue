<template>
  <div class="content_wrapper">
    <img
      :src="require('../assets/pokemons/' + `${code.obs_code}.png`)"
      alt=""
    >
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  name: 'Flag',
  props: {
    code: Object,
    default () {
      return {}
    }
  },
  data () {
    return {
    }
  },
  methods: {
  },
  computed: {
    ...mapState({
      flags: ({ flags }) => flags,
    })
  }
};
</script>

<style lang="scss" scoped>
.content_wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  i {
    font-size: 12rem;
  }
}


// Basic Mobile Setting
@media only screen and (min-width: 320px) and (max-width: 479px) {
  .content_wrapper {
    i {
      font-size: 9rem;
    }
  }
}
// For mobile (landscape)
@media only screen and (min-width: 480px) and (max-width: 767px) {
  .content_wrapper {
    i {
      font-size: 9rem;
    }
  }
}

img {
  width: 180px;
}
</style>
