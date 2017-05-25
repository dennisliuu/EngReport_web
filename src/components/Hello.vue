<template>
  <div class="hello animated fadeInUp">
    <p></p>
    <div class="hr1"> </div>
    <div class="ul">

      <a class="btn1" href="#about">
        <div class="li1">
          About
        </div>
      </a>
      <a class="btn1" href="#info">
        <div class="li1">Info</div>
      </a>
      <a class="btn1" href="#resource">
        <div class="li1">Resource</div>
      </a>
    </div>

    <div class="hr1"></div>

    <p></p>

    <el-row>
      <el-col :span="24">
        <div class="grid-content wow fadeInUp animated animated">
          <div class="about" id="about">
            <div class="container">
              <div class="col-md-6">
                <div class="clearfix"> </div>
              </div>
              <div class="col-md-6">
                <h3 class="wow fadeInLeft animated animated title" data-wow-delay=".5s">About</h3>
                <h4 class="wow fadeInLeft animated animated text" data-wow-delay=".5s">Once upon a time, a young man have an idea, maybe there is a better way to learn English, and the journey
                  has begun...</h4>
              </div>
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
              <div class="col-md-6">
                <h3 class="wow fadeInLeft animated animated title" data-wow-delay=".5s">Info</h3>
                <h4 class="wow fadeInLeft animated animated text" data-wow-delay=".5s">Once upon a time, an young man have an idea, maybe there is a better way to learn English, and the journey
                  has begun...</h4>
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
          <div class="about" id="resource">
            <div class="container">
              <div class="col-md-6">
                <div class="clearfix"> </div>
              </div>
              <div class="col-md-6">
                <h3 class="wow fadeInLeft animated animated title" data-wow-delay=".5s">About</h3>
                <h4 class="wow fadeInLeft animated animated text" data-wow-delay=".5s">Once upon a time, an young man have an idea, maybe there is a better way to learn English, and the journey
                  has begun...</h4>
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
</style>