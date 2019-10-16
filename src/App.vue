<template>
  <div id="app">
    <img v-if="imgUrl" alt="Vue logo" :src="imgUrl">
    <img v-else="" alt="Vue logo" src="@/assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  
  components: {
    HelloWorld
  },

  data(){
    return{
      imgUrl: ''
    }
  },

  created(){
    this.imgUrl = process.env.VUE_APP_IMG_URL;
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
