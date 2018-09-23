<template>
  <div id="app" @scroll="getScrollPosition">
    <app-home></app-home>
    <app-about></app-about>
    <app-services></app-services>
  </div>

</template>

<script>
import Home from './components/Home.vue';
import About from './components/About.vue';
import Services from './components/Services.vue';

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
    'app-about': About,
    'app-services': Services

  }
}
</script>

<style lang="scss">
@import './assets/sass/layout/_grid.scss';
@import './assets/sass/base/_reset.scss';
@import './assets/sass/base/_typography.scss';
@import './assets/sass/base/_utilities.scss';
@import './assets/sass/components/_button.scss';
@import './assets/sass/components/_card.scss';
@import './assets/sass/components/_heading.scss';



</style>
