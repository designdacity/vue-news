<template lang="html">
  <div v-show="isShowAbout" class="container">
    <transition name="slide">
       <div class="msg">
        <i @click="showAbout" class="close"></i>
        <div class="title">
          <h2>关于作品</h2>
          <h3>vue.js全家桶之腾讯新闻</h3>
        </div>
        <div class="content">
          <p class="tech"><b>技术栈</b></p>
          <div class="skill">axios(发起请求)<br>Vuex(状态共享)<br>vue-router(前端路由)<br>Vue2<br>SASS(SCSS)<br>Express(node.js)<br>ES6<br>localStorage<br>Webpack<br>CSS3<br>HTML5</div>
        </div>
        <div class="link">
          <p class="url"><b>源码地址:</b>&nbsp&nbsp&nbsp<a href="https://github.com/designdacity" target="_blank">designdacity</a></p>
        </div>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'about',
  data () {
    return {

    }
  },
  computed: {
    isShowAbout() {
      // console.log(this.$store.state.isShowAbout)
      return this.$store.state.isShowAbout;
    }
  },
  methods: {
    showAbout() {
      this.$store.commit('showAbout', false)
    }
  }
}
</script>

<style lang="css" scoped>
.msg {
  position: fixed;
  top: 60px;
  left: 0;
  bottom: 0;
  right: 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items:flex-start;
  z-index: 11;
  width: 75%;
  height: 330px;
  border-radius: 10px;
  box-shadow: 0 0 22px gray;
  margin: 10% 10%;
  overflow: auto;
  background: white;
  padding-left: 35px;
}
.close {
  position: absolute;
  z-index: 100;
  display: inline-block;
  width: 20px;
  height: 20px;
  background: url('../assets/close.png');
  background-repeat: no-repeat;
  background-size: contain;
  top: 2%;
  right: 2%;
}
.title {
  flex: 1;
}
.content {
  flex: 4;
}
.link {
  flex: 2.5;
}
h2 {
  display: block;
  text-align: center;
  margin: 15px 20px;
  color: red;
}
h3 {

  display: inline-block;
  opacity: .6;
  margin-bottom: 10px;
}
.url {
  padding-bottom: 10px;
}
</style>
