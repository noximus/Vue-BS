<template>
  <div id="app">
    <h1>Welcome to Protitorio</h1>
    <router-view/>
  </div>
</template>

<script>
import LandingPage from './components/LandingPage'
import MainContent from './components/MainContent'
export default {
  name: 'App',
  components: {
    LandingPage,
    MainContent
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
