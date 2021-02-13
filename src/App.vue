<template>
  <div id="app">
       <FirstProject></FirstProject>
  </div>
</template>

<script>


import FirstProject from "./components/FirstProject";

export default {
  name: 'App',
  components: {
     FirstProject
  }
}
</script>

<style>

body{
  background-image: url('components/bg1.jpg');
  background-size: cover;
  background-repeat: no-repeat;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 100px;
}
</style>
