<template>
  <div class="hello">
    <el-row>
      <el-col :span="24">
        <div class="grid-content wow fadeInUp animated animated">
          <div class="about" id="about">
            <div class="container">
              <div class="col-md-6">
                <div class="clearfix"> </div>
              </div>
              <div class="row">
                <div class="col-md-6">
                  <h3 class="wow fadeInLeft animated animated title" data-wow-delay=".5s">About</h3>
                  <h4 class="wow fadeInLeft animated animated text" data-wow-delay="1s">Once upon a time, a young man have an idea, maybe there is a better way to learn English, and the journey
                    has begun...</h4>
                </div>
                <div class="col-md-6">
                  <div class="hover column">
                    <div>
                      <figure><img src="../assets/pic1.svg"/></figure>
                    </div>
                  </div>
                </div>
              </div>
              <p></p>
              <div class="clearfix"> </div>
            </div>
          </div>
        </div>
      </el-col>
      <el-col :span="24">
        <div class="grid-content wow fadeInUp animated animated">
          <div class="about" id="info">
            <div class="container">
              <div class="col-md-6">
                <div class="clearfix"> </div>
              </div>
              <div class="col-md-12">
                <h3 class="wow fadeInLeft animated animated title" data-wow-delay=".5s">Info</h3>
                <h6 class="wow fadeInLeft animated animated text" data-wow-delay="1s">
                  <p>英文報章分享</p>

                  <p>時間:星期二加星期三中間空堂</p>

                  <p>地點:三教空教室(暫定)</p>

                  <p>內容:一周準備一篇文章(報章新聞雜誌皆可) 利用充分時間將文章內不熟的單字及文法作筆記(單 字可用電子檔印出) (用螢光筆畫記兩份:自己看到別人也看的到) 準備兩道問答題測驗對方有無看懂文意 必要時翻譯文章內容
                    並列印雙份文件保存。
                  </p>

                  <p>方式:雙方將不會的單字及文法弄懂後 準備方開始朗讀文章(注意段落及語氣) 閱讀後讓對方自行吸收約10min 開始問答題(no Chinese) 會後檢討對方的優缺點 之後隨著程度上升調整文章篇數 一次要比一次好
                    我們的目標就是希望能把英文學好、精通英文。 一起加油！
                  </p>
                </h6>
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3614.7599692877966!2d121.53330425066187!3d25.042218644037117!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3442a97d14c16483%3A0xf9ec3b549c4d6dbf!2z5ZyL56uL6Ie65YyX56eR5oqA5aSn5a24!5e0!3m2!1szh-TW!2stw!4v1495694272159"
                  width="600" height="450" frameborder="0" style="border:0" allowfullscreen></iframe>
                <p></p>
              </div>
              <div class="clearfix"> </div>
            </div>
          </div>
        </div>
      </el-col>
      <el-col :span="24">
        <div class="grid-content wow fadeInUp animated animated">
          <div class="about" id="join">
            <div class="container">
              <div class="col-md-6">
                <div class="clearfix"> </div>
              </div>
              <div class="row">
                <div class="col-md-6">
                  <h3 class="wow fadeInLeft animated animated title" data-wow-delay=".5s">Join</h3>
                  <h4 class="wow fadeInLeft animated animated text" data-wow-delay="1s">
                    <p>Come on and submit your subject!! </p>
                    <p>It will be fun !!</p>
                  </h4>
                </div>
                <div class="col-md-6">
                  <h4 class="wow fadeInLeft animated animated text" data-wow-delay="1s">
                    <iframe src="https://docs.google.com/forms/d/e/1FAIpQLScjOhRDawELnEa0cls-EY4aHYSUHdXRbtyemae8CFU7wErPuA/viewform?embedded=true"
                      width="100%" height="960" frameborder="0" marginheight="0" marginwidth="0">載入中…</iframe>
                  </h4>
                </div>
              </div>
              <div class="clearfix"> </div>
            </div>
          </div>
        </div>
      </el-col>
      <el-col :span="24">
        <div class="grid-content wow fadeInUp animated animated">
          <div class="about" id="Resource">
            <div class="container">
              <div class="col-md-6">
                <div class="clearfix"> </div>
              </div>
              <div class="row">
                <div class="col-md-6">
                  <h3 class="wow fadeInLeft animated animated title" data-wow-delay=".5s">Resource</h3>
                  <h4 class="wow fadeInLeft animated animated text" data-wow-delay="1s">
                    <p>All Resource can be found here !</p>
                  </h4>
                </div>
                <div class="col-md-6">
                  <h4 class="wow fadeInLeft animated animated text" data-wow-delay="1s">
                    <iframe src="https://docs.google.com/spreadsheets/d/14WHtQNdTIJznEj_rSzYi4_lh9FamGizR83GkFW5PdUE/pubhtml?widget=true&amp;headers=false" width="100%" height="100%"></iframe>
                  </h4>
                </div>
              </div>
              <div class="clearfix"> </div>
            </div>
          </div>
        </div>
      </el-col>

    </el-row>
  </div>
</template>

<script>
  import Firebase from 'firebase'
  import $ from 'jquery'
  var config = {
    apiKey: "AIzaSyDGJYONggbsDhXsEyYvdWVgcb55RTtD-Uc",
    authDomain: "engrp-d185a.firebaseapp.com",
    databaseURL: "https://engrp-d185a.firebaseio.com",
    projectId: "engrp-d185a",
    storageBucket: "engrp-d185a.appspot.com",
    messagingSenderId: "728270283768"
  };

  var firebaseApp = Firebase.initializeApp(config)
  var db = firebaseApp.database()

  export default {
    name: 'hello',
    data() {
      return {
        visible: false
      }
    },
    firebase: function () {
      return {
        Reports: db.ref('Reports')
      }
    },
    methods: {
      goto(e) {
        console.log(e)
        $('html, body').animate({
          scrollTop: $("#info").offset().top
        }, 1000);
      }
    }
  }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  @import url(animate.css);
  @import url(basic.css);
  @import url(element.css);

  .hover figure img {
    opacity: 1;
    -webkit-transition: .3s ease-in-out;
    transition: .3s ease-in-out;
  }

  .hover figure:hover img {
    opacity: .5;
  }

  .column {
    margin: 15px 15px 0;
    padding: 0;
  }

  .column::after {
    content: '';
    clear: both;
    display: block;
  }

  .column div {
    position: relative;
    float: left;
    width: 300px;
    height: 200px;
    margin: 0 0 0 25px;
    padding: 0;
  }

  figure {
    width: 300px;
    height: 200px;
    margin: 0;
    padding: 0;
    background: #fff;
    overflow: hidden;
  }
</style>