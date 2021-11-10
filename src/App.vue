<template>
  <HelloWorld msg="Welcome to Your Calculator"/>
  <get-request/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import GetRequest from "./components/GetRequest";

export default {
  name: 'App',
  components: {
    HelloWorld,
    GetRequest
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
