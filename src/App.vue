<template>
  <div id="app" @scroll="getScrollPosition">
    <app-home></app-home>
    <app-about></app-about>
  </div>

</template>

<script>
import Home from './components/Home.vue';
import About from './components/About.vue';
import {eventBus} from './main.js';

export default {

  data() {
    return {
      position: 0
    }
  },

  methods: {
    getScrollPosition(e) {

      let currentPosition = e.srcElement.scrollingElement.scrollTop;

      eventBus.$emit('position', currentPosition);
    }
  },

  created () {
      window.addEventListener('scroll', this.getScrollPosition);
    },

  destroyed () {
      window.removeEventListener('scroll', this.getScrollPosition);
     },

  components: {
    'app-home': Home,
    'app-about': About

  }
}
</script>

<style lang="scss">
@import './assets/sass/layout/_grid.scss';
@import './assets/sass/base/_reset.scss';
@import './assets/sass/base/_typography.scss';

</style>
