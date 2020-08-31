<template>
  <div id="todolist">
    <ul>
      <li v-for="todo in todos"
          :key="todo.id">{{ todo.info }}
      </li>
    </ul>
    <input type="text" v-model='newTodo' placeholder="Add Todo Here">
    <button type="submit" @click="addTodo">Add Todo</button>
  </div>
</template>

<script>

export default {
  data() {
    return {
      newTodo: '',
      todos: [
        { id: 0, info: 'Clean Room' },
        { id: 1, info: 'Practice Guitar' },
        { id: 2, info: 'Brush Teeth' }
      ]
    }
  },
  methods: {
    viewTodos() {
      console.log(this.newTodo);
    },
    addTodo() {
      this.todos.push({ id: this.todos.length, info: this.newTodo });

      console.log(this.todos);
    },
    removeTodo() {

    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  div {
    text-align: center;
  }
  li {
    list-style: none;
  }
</style>
