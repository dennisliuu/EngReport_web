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
                      <figure><img src="../assets/pic1.svg" /></figure>
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

                  <p>地點:三教空教室</p>

                  <p>內容:一周準備一篇文章(報章新聞雜誌皆可) 利用充分時間將文章內不熟的單字及文法作筆記(單 字可用電子檔印出) (用螢光筆畫記兩份:自己看到別人也看的到) 準備兩道問答題測驗對方有無看懂文意 必要時翻譯文章內容
                    並列印雙份文件保存。
                  </p>

                  <p>方式:雙方將不會的單字及文法弄懂後 準備方開始朗讀文章(注意段落及語氣) 學習進行全程錄音 可以保存起來當作未來檢討依據 閱讀後讓對方自行吸收約10min 開始問答題(no Chinese) 會後檢討對方的優缺點 之後隨著程度上升調整文章篇數 一次要比一次好
                    我們的目標就是希望能把英文學好、精通英文。 一起加油！
                  </p>
                </h6>
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3614.7599692877966!2d121.53330425066187!3d25.042218644037117!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3442a97d14c16483%3A0xf9ec3b549c4d6dbf!2z5ZyL56uL6Ie65YyX56eR5oqA5aSn5a24!5e0!3m2!1szh-TW!2stw!4v1495694272159"
                  width="100%" height="300px" frameborder="0" style="border:0"></iframe>
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

                    <div style="margin: 20px;"></div>
                    <el-form :model="numberValidateForm" ref="numberValidateForm" label-width="100px" class="demo-ruleForm">
                      <el-form-item label="Date">
                        <el-date-picker v-model="numberValidateForm.date" type="date" format="MM-dd" placeholder="Choose a date" :picker-options="pickerOptions0">
                        </el-date-picker>
                      </el-form-item>
                      <el-form-item label="Subject" prop="sub" :rules="[
                          { required: true, message: '不能為空'}
                        ]">
                        <el-input type="sub" v-model.number="numberValidateForm.sub" placeholder="What's Your Subject?" auto-complete="off"></el-input>
                      </el-form-item>

                      <el-form-item label="link" prop="link" :rules="[
                          { required: true, message: '不能為空'}
                        ]">
                        <el-input type="link" v-model="numberValidateForm.link" placeholder="Please remove https://" auto-complete="off">
                          <template slot="prepend">Http://</template>
                        </el-input>
                      </el-form-item>

                      <el-form-item>
                        <el-button type="primary" @click="submitForm('numberValidateForm')">提交</el-button>
                        <el-button @click="resetForm('numberValidateForm')">重置</el-button>
                      </el-form-item>
                    </el-form>
                    <!--<iframe src="https://docs.google.com/forms/d/e/1FAIpQLScjOhRDawELnEa0cls-EY4aHYSUHdXRbtyemae8CFU7wErPuA/viewform?embedded=true"
                      width="100%" height="960" frameborder="0" marginheight="0" marginwidth="0">載入中…</iframe>-->
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
          <div class="about" id="recored">
            <div class="container">
              <div class="col-md-6">
                <div class="clearfix"> </div>
              </div>
              <div class="row">
                <div class="col-md-6">
                  <h3 class="wow fadeInLeft animated animated title" data-wow-delay=".5s">Recored</h3>
                  <h4 class="wow fadeInLeft animated animated text" data-wow-delay="1s">
                    <p>All Recored can be found here !</p>
                    <p><a href="./words/" style="color: #365473">Words</a></p>
                  </h4>
                </div>
                <div class="col-md-6">
                  <h4 class="wow fadeInLeft animated animated text" data-wow-delay="1s">
                    <div style="margin: 20px;"></div>
                    <el-table :data="Reports" border stripe style="width: 100%" :default-sort="{prop: 'date', order: 'descending'}">
                      <el-table-column prop="sub" label="Subject" align="center" sortable>
                      </el-table-column>
                      <el-table-column prop="date" label="Date" align="center" sortable>
                      </el-table-column>
                      <el-table-column prop="link" label="Link" align="center" sortable>
                        <template scope="scope">
                          <el-button
                            @click.native.prevent="openurl(scope.row.link)"
                            type="text"
                            size="small">
                            Link
                          </el-button>
                        </template>
                      </el-table-column>
                    </el-table>
                    <!--<iframe src="https://docs.google.com/spreadsheets/d/14WHtQNdTIJznEj_rSzYi4_lh9FamGizR83GkFW5PdUE/pubhtml?widget=true&amp;headers=false"
                      width="100%" height="100%"></iframe>-->
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
  let config = {
    apiKey: "AIzaSyDGJYONggbsDhXsEyYvdWVgcb55RTtD-Uc",
    authDomain: "engrp-d185a.firebaseapp.com",
    databaseURL: "https://engrp-d185a.firebaseio.com",
    projectId: "engrp-d185a",
    storageBucket: "engrp-d185a.appspot.com",
    messagingSenderId: "728270283768"
  };

  let firebaseApp = Firebase.initializeApp(config)
  let db = firebaseApp.database()
  let reportsRef = db.ref('Reports')

  export default {
    name: 'hello',
    data() {
      return {
        visible: false,
        numberValidateForm: {
          sub: '',
          date: '',
          link: ''
        },
        pickerOptions0: {
          disabledDate(time) {
            return time.getTime() < Date.now() - 8.64e7;
          }
        }
      }
    },
    firebase: function () {
      return {
        Reports: reportsRef
      }
    },
    methods: {
      submitForm(formName) {
        var chooseDate = String(this.numberValidateForm.date).split(' ')
        this.numberValidateForm.date = chooseDate[1] + '-' + chooseDate[2]
        this.$refs[formName].validate((valid) => {
          if (valid) {
            reportsRef.push(this.numberValidateForm)
            this.$message({
              type: 'info',
              message: `action: Submit`
            });
          } else {
            this.$refs[formName].resetFields();
            console.log('error submit!!');
            return false;
          }
        });
        this.$refs[formName].resetFields();
      },
      resetForm(formName) {
        this.$refs[formName].resetFields();
      },
      openurl(url) {
        url = url.replace("https://","")
        window.open('https://' + url)
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