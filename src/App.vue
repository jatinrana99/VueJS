<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <Test/>
  <Event/>
  
  <h3>Passing data in a Child Components</h3>
  <Child name = "jatin Rana"  :user="user" :info="info"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Test from './components/Test.vue'
import Event from './components/Event.vue'
import Child from './components/Child.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Test,
    Event,
    Child
  },
  data(){
    return {
      user: {
        name:'Developer' , email:'dev@hotmail.com'
      }
    }
  },
  methods:{
    info(){
      console.warn("Parent function call")
      alert("How are you ?")
    }
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
