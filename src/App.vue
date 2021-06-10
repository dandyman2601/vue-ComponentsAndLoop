<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">    
    <Green></Green>
    <Blue></Blue>
    <Red></Red>
    <Yellow></Yellow>
    
    <div v-for="(item) in arrayData" :key="item">
      <div v-if="!(item%2)"><h1>{{item}} is an {{even}} number</h1></div>
      <div v-if="item%2"><h1>{{item}} is an {{odd}} number</h1></div>      
    </div>
  </div>
</template>

<script>
import Green from './components/Green.vue'
import Blue from './components/Blue.vue'
import Red from './components/Red.vue'
import Yellow from './components/Yellow.vue'

export default {
  name: 'App',
  components: {    
    Green,
    Blue,
    Red,
    Yellow
  },
  data () {
    return {
      arrayData: [100,3,10,9,30,3,6],
      even: "EVEN",
      odd: "ODD"

    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;  
  margin-top: 60px;
}
</style>
