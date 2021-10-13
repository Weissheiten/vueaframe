<template>
  <div id="app">
    <MyScene msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import MyScene from './components/MyScene.vue'

export default {
  name: 'App',
  components: {
    MyScene
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
