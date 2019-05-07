<template>
  <div id="app">
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
      newTodoText: "",
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
}
</style>
