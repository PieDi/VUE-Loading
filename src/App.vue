<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App--------"/>
    <vue-loading type="bars" color="yellow" :size="{ width: '50px', height: '50px' }"></vue-loading>    
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import {vueLoading} from './components/Loading'
export default {
  name: 'App',
  components: {
    HelloWorld,
    vueLoading
  },
  created() {
    console.log('----', vueLoading)
  },
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
