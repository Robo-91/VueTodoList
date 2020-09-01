<template>
  <div id="todolist">
    <ul>
      <li v-for="(todo, index) in todos"
          :key="index">{{ todo.info }}
          <button @click="removeTodo(index)">X</button>
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
        { info: 'Clean Room' },
        { info: 'Practice Guitar' },
        { info: 'Brush Teeth' }
      ]
    }
  },
  methods: {
    viewTodos() {
      console.log(this.newTodo);
    },
    addTodo() {
      const todoObj = { info: this.newTodo };
      this.todos.push(todoObj);

      console.log(this.todos);
    },
    removeTodo(index) {
      this.todos.splice(index, 1);
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
