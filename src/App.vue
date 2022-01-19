<template>
  <vue100vh :css="{ height: '100rvh' }" id="app">
    <div class="loading">
      <div class="animation">
        <img src="./assets/halloween_pumpkin1.png" />
        <img src="./assets/halloween_pumpkin2.png" />
        <img src="./assets/halloween_pumpkin3.png" />
      </div>
    </div>
    <Header />
    <router-view />
    <Footer />
  </vue100vh>
</template>

<script>
import vue100vh from 'vue-100vh'
import $ from 'jquery'

import Header from './components/Header.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    vue100vh,
    Header,
    Footer,
  },
  mounted: function () {
    $(function () {
      $(window).on('load', function () {
        $('body').addClass('disableScroll')
        $('.loading').delay(3000).fadeOut(300)
        $('body')
          .delay(3300)
          .queue(function () {
            $(this).removeClass('disableScroll')
          })
      })
      // eslint-disable-next-line no-unused-vars
      function stopload() {
        $('.loading').delay(2600).fadeOut(700)
      }
      setTimeout('stopload()', 10000)
    })
  },
}
</script>

<style>
body {
  margin: 0;
  background-image: url('./assets/back-img.png');
  background-size: 60%;
  background-repeat: repeat;
  overflow-x: hidden;
}
#app {
  font-family: '游明朝体', 'YuMincho', Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
.loading {
  position: fixed;
  width: 100vw;
  height: 100vh;
  top: 0px;
  left: 0px;
  background: #000;
  z-index: 9999;
}

.animation {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  display: flex;
  align-items: center;
  justify-content: center;
}
.animation img {
  width: min(10vw, 70px);
  margin: 0 2px;
}
.animation img {
  animation: load 1s infinite ease-in-out;
}

/* .animation:before,
.animation:after {
  position: absolute;
  top: 0;
  content: '';
} */

.animation img:nth-of-type(1) {
  animation-delay: 0s;
}
.animation img:nth-of-type(2) {
  animation-delay: 0.2s;
}
.animation img:nth-of-type(3) {
  animation-delay: 0.4s;
}

@keyframes load {
  0%,
  80%,
  100% {
    transform: scale(0.8);
    opacity: 0.8;
  }
  40% {
    transform: scale(1);
    opacity: 1;
  }
}
.disableScroll {
  overflow-y: hidden !important;
}
</style>
