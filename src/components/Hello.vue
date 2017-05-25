<template>
  <div class="hello animated fadeInUp">
    <p></p>
    <div class="hr1"> </div>
    <div class="ul">
      <div class="li1">
        <a class="btn1" href="#about" target="_parent">About</a>
      </div>
      <div class="li1">
        <a class="btn1" href="#info" target="_parent">Info</a>
      </div>
      <div class="li1">
        <a class="btn1" href="#resource">Resource</a>
      </div>
    </div>
    <div class="hr1"></div>
    <p></p>

    <el-row>
      <el-col :span="24">
        <div class="grid-content">
          <div class="about" id="about">
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

    <el-row>
      <el-col :span="24">
        <div class="grid-content">
          <div class="about" id="info">
            <div class="container">
              <div class="col-md-6">
                <div class="clearfix"> </div>
              </div>
              <div class="col-md-6">
                <h3 class="wow fadeInLeft animated animated title" data-wow-delay=".5s">Info</h3>
                <h4 class="wow fadeInLeft animated animated text" data-wow-delay=".5s">Once upon a time, an young man have an idea, maybe there is a better way to learn English, and the journey
                  has begun...</h4>
              </div>
              <div class="clearfix"> </div>
            </div>
          </div>
        </div>
      </el-col>
    </el-row>
    <el-row>
      <el-col :span="24">
        <div class="grid-content">
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

    <!--<el-button @click="visible = true">按钮</el-button>
                  <el-dialog v-model="visible" title="Hello world">
                    <p>欢迎使用 Element</p>
                    <div v-for="report in Reports" :key="report" :md-item="report">
                      {{ report.Sub }}
                    </div>
                  </el-dialog>-->
  </div>
</template>

<script>
  import Firebase from 'firebase'

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
  }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  @import url(animate.css);
  @import url(basic.css);
  @import url(element.css);
</style>