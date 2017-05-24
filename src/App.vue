<template>
  <div id="app">
    <!--<img src="./assets/logo.png">-->
  
    <section class="blur-container blur-7 justify-content-center align-items-center">
      <div class="blur-box">
        <div class="container-fluid d-flex justify-content-center align-items-center flex-column">
          <h2 class="text-uppercase">English as life</h2>
        </div>
      </div>
    </section>
  
    <hello></hello>
  
    <transition name="fade" mode="out-in">
      <button id="toTop" class="md-icon-button" @click.native="backTop" v-if="scrollPosition>200">
        <md-icon md-iconset="ion-arrow-up-b"></md-icon>
      </button>
    </transition>
  
  </div>
</template>

<script>
import $ from 'jquery'
import Hello from './components/Hello'
export default {
  name: 'app',
  components: {
    Hello
  },
  methods: {
    backTop() {
      $('html, body').animate({ scrollTop: 0 }, 500)
      return false
    },
    updateScroll() {
      this.scrollPosition = window.scrollY
    }
  },
  mounted: function () {
    window.addEventListener('scroll', this.updateScroll)
  }
}
</script>

<style>
#app {
  font-family: 'Quicksand', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /*margin-top: 60px;*/
}


/*basic*/

a {
  text-decoration: none !important;
  color: #fff;
}


/*banner*/

section {
  height: 70vh;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  position: relative;
}

.blur-container {
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
}

.blur-container::before,
.blur-container::after {
  top: 0px;
  left: 0px;
  content: '';
  width: 100%;
  height: 100%;
  display: block;
  position: absolute;
}

.blur-container .container-fluid {
  z-index: 10;
  width: 100%;
  height: 100%;
}

.blur-container .blur-box {
  display: block;
  position: relative;
}

.blur-container .blur-box::before,
.blur-container .blur-box::after {
  top: 0px;
  left: 0px;
  content: '';
  width: 100%;
  height: 100%;
  display: block;
  position: absolute;
}

.blur-container.blur-7 {
  --bg: url(https://zero-space.s3.amazonaws.com/photos/465f5d7c-bc67-47d4-b2de-b8597d716919.jpg);
  background-image: var(--bg);
}

.blur-container.blur-7 .blur-box {
  color: #fff;
  width: 100%;
  height: 90%;
  max-width: 600px;
  max-height: 400px;
}

.blur-container.blur-7 .blur-box::after {
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  opacity: 0.9;
  background-image: var(--bg);
  -webkit-filter: blur(6px) brightness(100%);
  filter: blur(6px) brightness(100%);
}

</style>
