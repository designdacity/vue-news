<template>
  <div id="app">
    <div>
      <router-view></router-view>
      <about></about>
    </div>
  </div>
</template>

<script>
import about from './page/about.vue';
export default {
  name: 'app',
  components: {
    about
  }
}
</script>

<style>
img {
  width: 100%;
}
html, body {
  overflow-x: hidden;
}
</style>
