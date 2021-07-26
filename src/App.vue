<template>
  <div id="app">
    <router-view/>
    <main-tabbar></main-tabbar>
  </div>
</template>

<script>
import MainTabbar from 'components/content/mainTabbar/MainTabar'

export default {
  name: 'App',
  components: {
    MainTabbar
  }
}
</script>

<style>
@import 'assets/css/base.css'; 
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
