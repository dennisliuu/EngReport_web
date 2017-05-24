<template>
  <div class="hello">
    <p></p>
    <div class="hr1"> </div>
    <div class="ul">
      <div class="li1">
        <a class="btn1" href="sp-about/about.html" target="_parent">About</a>
      </div>
      <div class="li1">
        <a class="btn1" href="sp-soap/soap.html" target="_parent">Info</a>
      </div>
      <div class="li1">
        <a class="btn1" href="../commitment.html">Resource</a>
      </div>
      <div class="li1">
        <a class="btn1" href="sp-contact/contact.html">Contact</a>
      </div>
    </div>
    <div class="hr1"></div>
    <p></p>
    
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

.container {
  font-size: 0px;
  max-width: 855px;
  margin-left: auto;
  margin-right: auto;
  align: center;
  background-color: #FFFFFF;
}

a.btn1 {
  text-decoration: none;
  font-family: cwTeXMing;
  color: #736357;
  background-color: transparent;
}

a.btn2 {
  text-decoration: none;
  font-family: cwTeXMing;
  color: #FFFFFF;
  background-color: #365473;
}

.block {
  display: inline-block;
  font-size: 18px;
  box-sizing: border-box;
  height: auto;
  text-align: center;
  padding: 0px;
  vertical-align: middle;
}
.block .icon {
  width: 25%;
  min-width: 200px;
}
.block .iconsmaill {
  display: inline-block;
  text-align: center;
  height: initail;
  width: 45px;
  min-width: 20px;
  padding-top: 30px;
  padding-bottom: 20px;
  background-color: #365473;
}
.block .fb {
  display: inline-block;
  margin-left: 5px;
  margin-right: auto;
}
.block .about10 {
  background-color: #FFFFFF;
  padding-top: 25px;
  padding-bottom: 20px;
}
.block .soap_03 {
  background-color: #FFFFFF;
  padding-top: 80px;
  padding-bottom: 0px;
  text-align: center;
  margin-left: 9px;
  margin-right: auto;
}
.block .soap_26 {
  background-color: #FFFFFF;
  padding-top: 0px;
  padding-bottom: 0px;
  text-align: center;
  margin-left: auto;
  margin-right: auto;
}

.li1 {
  display: inline-block;
  height: initail;
  width: 150px;
  font-family: "cwTeXMing", "Scheherazade";
  color: #736357;
  text-align: center;
  font-size: 17px;
  padding-top: 20px;
  padding-bottom: 20px;
}

.li1:hover {
  -webkit-transition-duration: 1s;
          transition-duration: 1s;
  background-color: #365473;
  color: #FFFFFF;
  cursor: pointer;
}

.li2 {
  text-align: center;
  background-color: #365473;
  color: #FFFFFF;
  font-family: "cwTeXMing";
  font-size: 18px;
  width: 100%;
  height: auto;
  padding-top: 35px;
  padding-bottom: 0px;
  margin-left: auto;
  margin-right: auto;
}

.li2:hover {
  color: #808080;
  -webkit-transition-duration: 0.5s;
          transition-duration: 0.5s;
  font-size: 19px;
  cursor: pointer;
}

.li3 {
  text-align: center;
  background-color: #365473;
  color: #736357;
  font-family: "cwTeXMing", "Scheherazade";
  font-size: 19px;
  width: 100%;
  height: auto;
  padding-top: 10px;
  padding-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
}

.li4 {
  text-align: center;
  background-color: #FFFFFF;
  color: #736357;
  font-family: "cwTeXMing", "Scheherazade";
  font-size: 14px;
  width: 100%;
  height: auto;
  padding-top: 10px;
  padding-bottom: 22px;
  margin-left: 0px;
  margin-right: 0px;
}

.li4:hover {
  text-decoration: underline;
  font-color: #red;
  -webkit-transition-duration: 1s;
          transition-duration: 1s;
}

.ul {
  width: 100%;
  text-align: center;
  vertical-align: middle;
}

.hr1 {
  border: solid 1px #736357;
  width: 855px;
  text-align: center;
  margin-left: auto;
  margin-right: auto;
}

.hr2 {
  border: solid 1px #736357;
  width: 100%;
  line-height: 500px;
  text-align: left;
  background-color: #FFFFFF;
  margin-left: auto;
  margin-right: auto;
}

.hr3 {
  border: solid 1px #736357;
  width: 739px;
  line-height: 0px;
  text-align: center;
  background-color: #FFFFFF;
  margin-left: auto;
  margin-right: auto;
}

p {
  padding-top: 10px;
  padding-bottom: 10px;
}

.tittle1 {
  background-color: transparent;
  font-family: "cwTeXMing", "Scheherazade";
  color: #736357;
  text-align: center;
  font-size: 16.8px;
  width: 100%;
  text-indent: 10px;
  padding-top: 10px;
  padding-bottom: 10px;
  margin-left: auto;
  margin-right: auto;
}

.btn {
  background-color: #FFFFFF;
  font-family: "cwTeXMing", "Scheherazade";
  font-weight: bold;
  color: #736357;
  text-align: center;
  font-size: 13.5px;
  width: auto;
  text-indent: 0px;
  padding-top: 12px;
  padding-bottom: 20px;
  margin-left: auto;
  margin-right: auto;
}

.btn:hover {
  -webkit-transition-duration: 1s;
          transition-duration: 1s;
  color: #808080;
  cursor: pointer;
}

.tittle3 {
  background-color: #FFFFFF;
  font-family: "cwTeXMing", "Scheherazade";
  color: #736357;
  text-align: left;
  font-size: 16.8px;
  width: 67.5%;
  padding-top: 0px;
  padding-bottom: 10px;
  padding-left: 0px;
  margin-left: auto;
  margin-right: auto;
}

.tittle4 {
  background-color: transparent;
  font-family: "Scheherazade";
  color: #736357;
  text-align: left;
  line-height: 40px;
  font-size: 30px;
  width: 67.5%;
  padding-top: 0px;
  padding-bottom: 0px;
  padding-left: 0px;
  margin-left: auto;
  margin-right: auto;
}

.about1 {
  line-height: 0px;
  background-color: transparent;
  font-family: "cwTeXMing", "Scheherazade";
  color: #736357;
  text-align: center;
  width: auto;
  font-size: 14px;
  text-indent: 10px;
  padding-top: 20px;
  padding-bottom: 6px;
  margin-left: auto;
  margin-right: auto;
}

.about2 {
  line-height: 0px;
  background-color: transparent;
  font-family: "cwTeXMing", "Scheherazade";
  color: #736357;
  text-align: center;
  font-size: 14px;
  text-indent: 10px;
  padding-top: 30px;
  padding-bottom: 6px;
  margin-left: auto;
  margin-right: auto;
}

.about3 {
  line-height: 0px;
  background-color: transparent;
  font-family: "cwTeXMing", "Scheherazade";
  color: #736357;
  text-align: center;
  font-size: 14px;
  text-indent: 10px;
  padding-top: 15px;
  padding-bottom: 60px;
  margin-left: auto;
  margin-right: auto;
}

.about4 {
  line-height: 20px;
  background-color: #FFFFFF;
  font-family: "cwTeXMing", "Scheherazade";
  color: #736357;
  text-align: justify;
  width: 67.5%;
  font-size: 13.5px;
  padding-top: 0px;
  padding-bottom: 10px;
  margin-left: auto;
  margin-right: auto;
}

.div.p1 {
  line-height: 25px;
  background-color: #FFFFFF;
  font-family: "cwTeXMing", "Scheherazade";
  color: #736357;
  text-align: left;
  font-size: 15px;
  text-indent: 3px;
  padding-top: 1px;
  padding-bottom: 6px;
}

.div.p2 {
  line-height: 50px;
  background-color: #FFFFFF;
  font-family: "cwTeXMing", "Scheherazade";
  color: #736357;
  text-align: left;
  font-size: 21px;
  text-indent: 3px;
  padding-top: 0px;
  padding-bottom: 0px;
}

.div.p3 {
  line-height: 31px;
  background-color: #FFFFFF;
  font-family: "cwTeXMing", "Scheherazade";
  color: #736357;
  text-align: left;
  font-size: 14.5px;
  text-indent: 3px;
  padding-top: 6px;
  padding-bottom: 1px;
  margin-left: auto;
  margin-right: auto;
}

div.p4 {
  line-height: 20px;
  background-color: #FFFFFF;
  font-family: "cwTeXMing", "Scheherazade";
  color: #736357;
  text-align: left;
  font-size: 16px;
  text-indent: 3px;
  padding-bottom: 10px;
}

div.p5 {
  line-height: 20px;
  background-color: #FFFFFF;
  font-family: "cwTeXMing", "Scheherazade";
  color: #736357;
  text-align: left;
  font-size: 14.5px;
  text-indent: 3px;
  padding-bottom: 7px;
}

.sp {
  background-color: #FFFFFF;
  padding-top: 10px;
  padding-bottom: 8px;
}

.iconsmaill2 {
  display: inline-block;
  background-color: #FFFFFF;
  padding-top: 50px;
  padding-bottom: 0px;
  margin-left: 320px;
  margin-right: auto;
}

.iconsmaill3 {
  display: inline-block;
  background-color: #FFFFFF;
  padding-top: 40px;
  padding-bottom: 0px;
  margin-left: -280px;
  margin-right: auto;
}

.c, .d, .e {
  background-color: #365473;
  height: initail;
}

.g {
  background-color: #FFFFFF;
  text-align: center;
}

.h {
  background-color: #FFFFFF;
  vertical-align: middle;
  text-align: left;
  padding-top: 45px;
  padding-bottom: 10px;
}

.i {
  background-color: #FFFFFF;
  vertical-align: middle;
  text-align: left;
  padding-top: 45px;
  padding-bottom: 10px;
}

.j {
  background-color: #FFFFFF;
}

.a {
  width: 100%;
}

.b {
  width: 100%;
  height: auto;
  background-color: transparent;
  background-image: url(http://www.inpindesign.com/SP/soap.jpg);
  background-repeat: no-repeat;
  background-position: 50%;
}

.b1 {
  width: 17%;
  height: auto;
  vertical-align: top;
  background-color: #FFFFFF;
  padding-top: 0px;
  padding-bottom: 0px;
}

.b2 {
  width: 3%;
  height: 130px;
  vertical-align: top;
  background-color: #FFFFFF;
  border-top: solid 1px #736357;
  border-bottom: solid 1px #736357;
  padding-top: 0px;
  padding-bottom: 0px;
}

.b3 {
  width: 10%;
  height: auto;
  vertical-align: top;
  background-color: #FFFFFF;
  border-top: solid 1px #736357;
  border-bottom: solid 1px #736357;
  padding-top: 25px;
  padding-bottom: 0px;
}

.b4 {
  width: 10%;
  height: auto;
  vertical-align: top;
  background-color: #FFFFFF;
  border-top: solid 1px #736357;
  border-bottom: solid 1px #736357;
  padding-top: 25px;
  padding-bottom: 0px;
}

.b5 {
  width: 10%;
  height: auto;
  vertical-align: top;
  background-color: #FFFFFF;
  border-top: solid 1px #736357;
  border-bottom: solid 1px #736357;
  padding-top: 25px;
  padding-bottom: 0px;
}

.b6 {
  width: 10%;
  height: auto;
  vertical-align: top;
  background-color: #FFFFFF;
  border-top: solid 1px #736357;
  border-bottom: solid 1px #736357;
  padding-top: 25px;
  padding-bottom: 0px;
}

.b7 {
  width: 10%;
  height: auto;
  vertical-align: top;
  background-color: #FFFFFF;
  border-top: solid 1px #736357;
  border-bottom: solid 1px #736357;
  padding-top: 25px;
  padding-bottom: 0px;
}

.b8 {
  width: 10%;
  height: auto;
  vertical-align: top;
  background-color: #FFFFFF;
  border-top: solid 1px #736357;
  border-bottom: solid 1px #736357;
  padding-top: 25px;
  padding-bottom: 0px;
}

.b9 {
  width: 3%;
  height: 130px;
  vertical-align: top;
  background-color: #FFFFFF;
  border-top: solid 1px #736357;
  border-bottom: solid 1px #736357;
  padding-top: 0px;
  padding-bottom: 0px;
}

.b10 {
  width: 17%;
  height: auto;
  vertical-align: top;
  background-color: #FFFFFF;
  padding-top: 0px;
  padding-bottom: 0px;
}

.soap1a {
  width: 100%;
  align: center;
  background-color: #FFFFFF;
  padding-top: 0px;
  padding-bottom: 0px;
}

.soap2a {
  text-align: center;
  width: 100%;
  vertical-align: top;
  background-color: #FFFFFF;
  padding-top: 0px;
  padding-bottom: 0px;
}

.soap3a {
  width: 100%;
  vertical-align: center;
  text-align: center;
  background-color: #FFFFFF;
}

.soap4a {
  width: 100%;
  vertical-align: top;
  text-align: center;
  background-color: #FFFFFF;
  padding-top: 50px;
  padding-bottom: 0px;
}

.soap5a {
  width: 855px;
  height: 150px;
  background-color: #FFFFFF;
}

.soap_interval6 {
  width: 855px;
  height: 100px;
  margin-left: auto;
  margin-right: auto;
  vertical-align: middle;
  background-color: #FFFFFF;
}

.f {
  width: 100%;
  height: auto;
}

.c {
  width: 34%;
  height: 200px;
}

.d, .e {
  width: 33%;
  height: 200px;
}

.g {
  width: 171px;
  height: 280px;
}

.h {
  width: 398px;
  height: 280px;
}

.i {
  width: 256px;
  height: 280px;
}

.j {
  width: 30px;
  height: 280px;
}

@media screen and (max-width: 800px) {
  .c, .b, .f, .li, .g, .i, .h, .index01, .index03 {
    width: 100%;
  }

  .e, .d {
    width: 50%;
  }

  .j {
    width: 0%;
  }

  .ul, .li1, img.soap_26, .hr1, .hr2, .hr3 {
    width: 100%;
  }

  .b1, .b2, .b9, .b10, .bj {
    width: 0%;
  }

  .b3, .b4, .b5, .b6, .b7, .b8 {
    width: 33%;
  }

  .soap1a, .block.soap2a, .soap3a, .soap4a, .soap5a {
    width: 100%;
  }
}
@media screen and (max-width: 400px) {
  .b, .c, .d, .e, .f, .li, .h, .i, .index01, .index03, .hr1, .hr2, .hr3 {
    width: 100%;
  }

  .b1, .b2, .b9, .b10, .bj {
    width: 0%;
  }

  .b3, .b4, .b5, .b6, .b7, .b8 {
    width: 33%;
  }

  .soap1a, .block.soap2a, .soap3a, .soap4a, .soap5a, img.soap_26 {
    width: 100%;
  }
}

</style>
