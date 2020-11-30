<template>
  <div id="app">
    <img src="./assets/logo.png">
    <Book/>
    <router-view/>
  </div>
</template>

<script>
import Book from './components/Book'

export default {
  name: 'App',
  components: {
    Book
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
