<template>
  <div id="app">
    <!--<img src="./assets/logo.png">-->
    <el-button @click="visible = true">按钮</el-button>
    <el-dialog v-model="visible" title="Hello world">
      <p>欢迎使用 Element</p>
      <div v-for="report in Reports" :key="report" :md-item="report">
        {{ report.Sub }}
      </div>
    </el-dialog>

    <hello></hello>
  </div>
</template>

<script>
import Hello from './components/Hello'
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
  name: 'app',
  data: function () {
    return { visible: false }
  },
  firebase: function () {
    return {
      Reports: db.ref('Reports')
    }
  },
  components: {
    Hello
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

</style>
