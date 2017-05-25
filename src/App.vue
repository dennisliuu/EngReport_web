<template>
  <div id="app">
    <!--<img src="./assets/logo.png">-->
    <header>
      <section class="blur-container blur-7 justify-content-center align-items-center">
        <div id="nav">
          <ul class="social-container header__item">
            <li class="social__icon social__icon--fb">
              <img src="https://s29.postimg.org/3ldyta4qb/image.png" alt="facebook">
            </li>
            <li class="social__icon social__icon--dr">
              <img src="https://s29.postimg.org/vqltn8fhv/image.png" alt="dribbble">
            </li>
            <li class="social__icon social__icon--in">
              <img src="https://s29.postimg.org/p1fa77u5v/image.png" alt="instagram">
            </li>
          </ul>
        </div>
        <div class="blur-box">
          <div class="container-fluid d-flex justify-content-center align-items-center flex-column">
            <h2 class="text-uppercase">English as life</h2>
          </div>
        </div>
      </section>
    </header>
    
    <hello></hello>

    <footer class="footer-distributed">
      <div class="footer-left">
        <p class="footer-company-name">Copyright &copy; Wei-zen Liu</p>
      </div>
      <div class="footer-right">
        <p class="footer-links">
          <a href="https://www.facebook.com/dennis.liu.5095" target="_blank">Facebook</a> ·
          <a href="https://www.google.com.tw/webhp?sourceid=chrome-instant&ion=1&espv=2&ie=UTF-8#q=%E7%94%B1%E6%AF%94%E6%BF%B1%E7%B5%90%E8%A1%A3&*"
            target="_blank">Wife</a>
        </p>
      </div>
    </footer>


    <transition name="fade" mode="out-in">
      <el-button id="toTop" type="text" icon="arrow-up" @click.native="backTop" v-if="scrollPosition>200"></el-button>
    </transition>

  </div>
</template>

<script>
  import $ from 'jquery'
  import Hello from './components/Hello'
  export default {
    name: 'app',
    data() {
      return {
        scrollPosition: null
      }
    },
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
  /* totop */

  #toTop {
    /*background-color: transparent;*/
    text-decoration: none;
    position: fixed;
    bottom: 20px;
    right: 2%;
    overflow: hidden;
    z-index: 9999;
    width: 32px;
    height: 28px;
    border: none;
    opacity: 0.3;
  }

  #toTop:hover {
    text-decoration: none;
    position: fixed;
    bottom: 20px;
    right: 2%;
    overflow: hidden;
    z-index: 9999;
    width: 32px;
    height: 28px;
    border: none;
    opacity: 1;
  }
  /*header*/

  #nav {
    position: fixed;
    z-index: 1000;
    top: 0;
    left: 0;
    width: 100%;
  }

  #nav ul {
    list-style: none;
  }

  #nav li {
    display: inline-block;
    padding: 10px;
  }

  .social-container {
    width: 7.25rem;
    list-style: none;
    overflow: hidden;
    padding: 0;
    margin: 0;
    float: right;
  }

  .social-container .social__icon {
    width: 1.5rem;
    float: left;
    cursor: pointer;
  }

  .social-container .social__icon.social__icon--dr {
    margin-left: 1.25rem;
  }

  .social-container .social__icon.social__icon--in {
    margin-left: 1.5rem;
  }

  .social-container .social__icon.social__icon--fb img {
    margin-right: 0 1.5rem;
  }
  /*banner*/

  section {
    height: 75vh;
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
  /*footer*/

  footer {
    bottom: 0;
  }

  @media (max-height:800px) {
    footer {
      position: static;
    }
  }

  .footer-distributed {
    background-color: rgb(238, 238, 238);
    /*background-image: url('../assets/footer.svg');*/
    background-repeat: no-repeat;
    background-size: cover;
    opacity: 0.8;
    box-shadow: 0 1px 1px 0 rgba(0, 0, 0, 0.12);
    box-sizing: border-box;
    width: 100%;
    text-align: left;
    padding: 60px 60px;
    overflow: hidden;
  }
  /* Footer left */

  .footer-distributed .footer-left {
    float: left;
  }

  .footer-distributed .footer-links {
    color: #fff;
    margin: 0 0 10px;
    padding: 0;
    position: relative;
  }

  .footer-distributed .footer-links a {
    display: inline-block;
    line-height: 1.8;
    text-decoration: none !important;
    color: #F3A3B7;
    font-size: 14px !important;
    font-weight: 700;
  }

  .footer-distributed .footer-links a:hover {
    display: inline-block;
    line-height: 1.8;
    text-decoration: none !important;
    color: #96C6EB;
    font-size: 14px !important;
    font-weight: 800;
    -webkit-transition: color 0.4s;
    -moz-transition: color 0.4s;
    transition: color 0.4s;
  }

  .footer-distributed .footer-company-name {
    color: #F3A3B7;
    font-size: 16px;
    font-weight: 800;
    margin: 0;
  }
  /* Footer right */

  .footer-distributed .footer-right {
    float: right;
  }
  /* media */

  @media (max-width: 800px) {
    .footer-distributed {
      padding: 30px;
      text-align: center;
    }
    .footer-distributed .footer-left,
    .footer-distributed .footer-right {
      float: none;
      max-width: 300px;
      margin: 0 auto;
    }
    .footer-distributed .footer-left {
      margin-bottom: 20px;
    }
  }
</style>