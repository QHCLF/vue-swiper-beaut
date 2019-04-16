<template>
  <div id="app">
<!--    <img alt="Vue logo" src="./assets/logo.png">-->
<!--    <HelloWorld msg="Welcome to Your Vue.js App"/>-->

      <swiperBeaut>
          <slide v-for="(item, index) in items" :index="index">
              <img :src="item.img">
          </slide>
      </swiperBeaut>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'

import swiperBeaut from './components/swiperBeau.vue'
import slide from './components/slide.vue'

export default {
  name: 'app',
  data(){
    return{
      items:[
          {img:require('./assets/1.jpeg')},
          {img:require('./assets/2.jpeg')},
          {img:require("./assets/3.jpeg")},
          {img:require("./assets/4.jpeg")},
          {img:require("./assets/5.jpeg")},

        ]
    }
  },
  components: {
    swiperBeaut,
      slide,
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
