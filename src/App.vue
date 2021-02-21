<template>
  <div id="app">
    <Navbar msg="Welcome to Your Vue.js App"/>
    <Dashboard msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import Dashboard from './components/Dashboard.vue'
import Navbar from './components/Navbar.vue'
export default {
  name: 'App',
  components: {
    Dashboard,
    Navbar
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #bababa;
  /* margin-top: 60px; */
}
.common-card,select {
    font-size: 12px;
     color: #bababa !important;
}
canvas{
  max-width: 100% !important;
}
</style>
