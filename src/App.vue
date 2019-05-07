<template>
  <div id="app">
    <h2>Vue TODOS</h2>
    <TodoList v-bind:todos="todos"></TodoList>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import TodoListItem from "./components/TodoListItem";
import TodoList from "./components/TodoList";

let nextTodoId = 0;

export default {
  name: "App",
  components: {
    HelloWorld,
    TodoListItem,
    TodoList
  },
  data() {
    return {
      todos: [
        {
          id: nextTodoId++,
          text: "Learn Vue"
        },
        {
          id: nextTodoId++,
          text: "Learn about single-file components"
        },
        {
          id: nextTodoId++,
          text: "Fall in love"
        }
      ]
    };
  }
};
</script>

<style>
body {
  padding: 50px;
  text-align: center;
}
input {
  width: 300px;
}
ul {
  text-align: left;
  padding-left: 100px;
}
</style>
