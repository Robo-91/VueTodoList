<template>
  <div id="todolist">
    <ul>
      <li v-for="(todo, index) in todos" :class="{ completed: todo.completed }"
          :key="index" ><input type='checkbox' v-model='todo.completed'>{{ todo.info }}
          <button class='delete' @click="removeTodo(index)">X</button>
      </li>
      
    </ul>
    <input class='new-todo' type="text" v-model='newTodo' placeholder="Add Todo Here">
    <button class='add' type="submit" @click="addTodo">Add Todo</button>
  </div>
</template>

<script>

export default {
  data() {
    return {
      newTodo: '',
      completed: false,
      todos: [
        { info: 'Clean Room' },
        { info: 'Practice Guitar' },
        { info: 'Brush Teeth' }
      ]
    }
  },
  methods: {
    addTodo() {
      const todoObj = { info: this.newTodo };
      this.todos.push(todoObj);
      this.newTodo = '';
    },
    removeTodo(index) {
      this.todos.splice(index, 1);
    }
  }
}



</script>

<style scoped>
  div {
    text-align: center;
  }
  ul {
    padding-inline-start: 0;
  }
  li {
    list-style: none;
    padding: 1.3em;
    display: flex;
    justify-content: space-between;
    margin: 1.5em 1em 1.5em 1em;
    box-shadow: 0px 0px 20px -7px rgba(69,69,69,0.8);
    border-radius: 10px;
  }
  .delete {
    background-color: crimson;
    border: none;
    border-radius: 50%;
    color: white;
    font-weight: bolder;
    width: 22px;
  }
  .delete:hover {
    background-color:lightcoral;
    transition: .2s;
  }
  .add {
    margin: 1em;
    color: white;
    background-color: #5bc0de;
    border: none;
    border-radius: 10px;
    width: 12em;
    height: 2em;
    font-weight: bolder;
  }
  .add:hover {
    box-shadow: inset 0px 0px 50px -27px rgba(0,0,0,1);
  }
  .completed {
    text-decoration: line-through;
  }
</style>
