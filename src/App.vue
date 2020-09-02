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
  margin: 60px auto auto auto;
  width: 35em;
}
button {
  cursor: pointer;
  outline: none;
}
.new-todo {
  text-align: center;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  box-shadow: 0px 0px 7px 0px rgba(102,102,102,0.75);
  display: block;
  margin: 3em auto 1em auto;
  border: none;
  border-radius: 10px;
  width: 23em;
  height: 2.5em;
  outline: none;
}
</style>
