<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <Test/>
  <Event/>
  
  <h3>Passing data in a Child Components</h3>
  <Child name = "jatin Rana"  :user="user" :info="info"/>




  <!-- this is for users functions -->
  
    <li v-for="user in users" :key="user.id">
      {{ user.pos }}
      <User :data="user" :getName="getName"/>
<!-- {{ user.email }} -->
    </li>
  
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Test from './components/Test.vue'
import Event from './components/Event.vue'
import Child from './components/Child.vue'
import User from './components/User.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Test,
    Event,
    Child,
    User
  },
  data(){
    return {
      user: {
        name:'Developer' , email:'dev@hotmail.com'
      },
      // passing the data in the user component
      users: [
        {id:'01' , name:'raju' , email :'raju@gmail.com' , pos:'Vue Js Developer'},
        {id:'02' , name:'kaju' , email :'kaju@gmail.com' , pos:'Java Developer'},
        {id:'03' , name:'maju' , email :'maju@gmail.com',pos:'React Developer'},
        {id:'04' , name:'baju' , email :'baju@gmail.com',pos:'.Net Developer'},
    ]
    }
  },
  methods:{
    info(){
      console.warn("Parent function call")
      alert("How are you ?")
    },
    getName(name){
      alert(name)
      // ended here I am here
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
