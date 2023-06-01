<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld/>
  <Test/>
  <router-link to="/">Home</router-link>
  <br>
  <router-link to="/login">Login</router-link>
  <br>
  <router-link to="/profile">Profile</router-link>
  <br>
  <router-link to="/profile/Umar">Hi Umar Welcome</router-link>
  <br>
  <router-link to="/profile/Ram">Hi Ram Weclome</router-link>

  <button v-on:click="$router.push('/login')">Login Page</button>

  <router-view></router-view>

</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Test from './components/Test.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Test
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
