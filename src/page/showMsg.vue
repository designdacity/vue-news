<template lang="html">
  <div class="container">
    <div class="msg-header">
      <img src="../assets/back.png" @click="goback">
      <span>个人中心</span>
    </div>
      <div class="msg">
        <h2>雷毅</h2>
        <div class="target">
            <h3>求职意向：</h3>
            <p>web前端实习生</p>
        </div>
        <div class="background">
          个人信息：
          <p>学校：东华理工大学</p>
          <p>专业：软件工程(本科)</p>
          <p>年级：大三</p>
          <p>电话：18720795869</p>
        </div>
      </div>
      <div class="more">
        <p class="aa">其他信息：</p>
        <p class="bb">掘金栏：<a href="https://juejin.im/user/57f05a528ac24700587bf8bb" target="_blank">Designudacity</a></p>
        <p class="bb">github：<a href="https://github.com/designdacity" target="_blank">designdacity</a></p>
        <p class="bb">QQ：876649373</p>
        <p class="bb">邮箱：876649373@qq.com</p>
      </div>
    <div class="production">
      <div class="prox">
        <div class="top">
          <img src="../assets/jishu.png" alt="">
          <p class="pro_1">技术栈</p>
        </div>
        <div class="bottom">
          <p class="bat">【前端】Vue.js、CSS/CSS3、HTML/HTML5、JavaScript(ES6、ES5)、SASS(SCSS)、stylus、微信小程序</p>
          <p class="bat">【后端】Node.js(Express.js)</p>
          <p class="bat">【自动化构建】Webpack、Gulp</p>
          <p class="bat">【版本管理】Git</p>
        </div>
      </div>
      <div class="proy">
        <div class="top">
          <img src="../assets/zuopin.png" alt="">
          <p class="pro_1">作品</p>
        </div>
        <div class="bottom">
          vue.js全家桶之腾讯新闻
        </div>
      </div>
      <div class="summary">
        <div class="top">
          <img src="../assets/my_1.png" alt="">
          <p class="pro_1">简介</p>
        </div>
        <div class="bottom">
          &nbsp &nbsp&nbsp &nbsp我是一个软件工程专业的学生，在校学习了多门编程语言，本人爱好编程。有着较强的学习能力
          ，喜欢逛技术网站，爱好新技术，有良好的团队协作能力和沟通能力，希望找到一个喜欢的公司从实习开始做起。一直学习下去。
          坚信一句话，做人不将就，代码亦是如此！
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'showMsg',
  data () {
    return {

    }
  },
  computed: {
  },
  methods: {
     goback() {
      this.$router.go(-1)
    }
  }
}
</script>

<style lang="css" scoped>
/*.container {
  width: 100%;
  display: flex;
  position: relative;
  font-size: 12px;
  margin-top: 30px;
}*/
.msg-header {
  width: 100%;
  height: 1.33rem;
  background-color: #07a0ec;
  color: #fff;
  font-size: 16px;
  display: flex;
  align-items: center;
  position: fixed;
  top: 0;
  z-index:11;
}
.msg-header img {
  width: 25px;
  height: 25px;
  padding: 0 .19rem;
}
.msg {
  flex: 1;
  display: flex;
  flex-direction: column;
  position:relative;
  margin-top: 48px;
  background-color: #fbfbfb;
}
.more {
  margin-top: 10px;
  flex: 1;
}
P {
  margin-top: 5px;
}
h2{
  font-size: 18px;
}
h3{
  font-size: 16px;
}
.background {
  flex: 2;
}
.production {
  flex: 3;
  height: 480px;
  display: flex;
  flex-direction: column;
  color: black;
  font-size: 10px;
}
.aa {
  margin-bottom: 10px;
  font-size: 16px;
}
.bb {
  font-size: 14px;
}
a {
  text-decoration: none;
  font-size: 15px;
  color: #1397EC;
}
img {
  width: 25px;
  height: 25px;
}
.prox {
  flex: 4;
  margin-top: 5px;
  display: flex;
  flex-direction: column;
  border-bottom: 1px solid #CDCDCD;
}
.proy {
  flex: 3;
  margin-top: 5px;
  display: flex;
  flex-direction: column;
  border-bottom: 1px solid #CDCDCD;
}
.top {
  /*flex: 1;*/
  display: flex;
  color:red;
  height: 25px;
}
.bottom {
/*flex: 8;*/
padding: 8px 5px;
}
.summary {
  display: flex;
  flex-direction: column;
  flex: 4;
}
.pro_1 {
  padding-left: 5px

}
.bottom {
  margin-top: 6px;
  line-height: 18px;
}
</style>
