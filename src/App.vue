<template>
  <div id="app">
    <!--<img src="./assets/logo.png">-->
    <div class="container">
      <nav class="navbar navbar-toggleable-md navbar-light fixed-top">
        <button class="navbar-toggler navbar-toggler-right" style="z-index: 99999" type="button" data-toggle="collapse" data-target="#navbarNav"
          aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <div class="wow animated fadeInDown" style="width: 100%">
            <div class="hr1"> </div>
            <div class="ul">
              <a class="btn1" href="#about">
                <div class="li1">About</div>
              </a>
              <a class="btn1" href="#info">
                <div class="li1">Info</div>
              </a>
              <a class="btn1" href="#join">
                <div class="li1">Join</div>
              </a>
            </div>
            <div class="hr1"></div>
          </div>
        </div>
      </nav>
    </div>

    <!--<nav class="navbar fixed-top">
      <div class="wow animated fadeInDown">
        <div class="hr1"> </div>
        <div class="ul">
          <a class="btn1" href="#about">
            <div class="li1">About</div>
          </a>
          <a class="btn1" href="#info">
            <div class="li1">Info</div>
          </a>
          <a class="btn1" href="#join">
            <div class="li1">Join</div>
          </a>
        </div>
        <div class="hr1"></div>
      </div>
    </nav>-->

    <header>
      <section class="blur-container blur-7 justify-content-center align-items-center">
        <div class="blur-box">
          <div class="container-fluid d-flex justify-content-center align-items-center flex-column">
            <h2 class="text-uppercase">English as life</h2>
          </div>
        </div>
      </section>
    </header>

    <hello></hello>

    <transition name="fade" mode="out-in">
      <el-button id="toTop" type="text" icon="arrow-up" @click.native="backTop" v-if="scrollPosition>200"></el-button>
    </transition>

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
      window.addEventListener('scroll', this.updateScroll),
        $(window).scroll(function (evt) {
          if ($(window).scrollTop() > 0)
            // $(".navbar").removeClass("navbar-light");
            $(".navbar").css('background-color', '#f0f0f0');
          else
            $(".navbar").css('background-color', 'transparent');
        });
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
    background-image: url("https://s29.postimg.org/vho8xb2pj/landing_bg.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: bottom;
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
    z-index: 100;
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