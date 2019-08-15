<template>
  <div id="app" class="mt-0">
    <nav-bar></nav-bar>
    <router-view />
  </div>
</template>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>


<script>
  import NavBar from './components/NavBar'

export default {
  components: {
    NavBar
  }
}
</script>