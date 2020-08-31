<template>
  <div id="app">
    <heading></heading>
    <todos></todos>
  </div>
</template>

<script>
import heading from './components/heading.vue'
import todos from './components/todo.vue'

export default {
  name: 'App',
  components: {
    heading,
    todos
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
