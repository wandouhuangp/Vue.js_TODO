<template>
  <div>
    <input v-model="newTodoText" v-on:keydown.enter="addTodo">
    <ul v-if="todos.length">
      <TodoListItem
        v-for="todo in todos"
        v-bind:key="todo.id"
        v-bind:todo="todo"
        v-on:remove="removeTodo"
      ></TodoListItem>
    </ul>
    <p v-else>No todo!</p>
  </div>
</template>

<script>
import TodoListItem from "./TodoListItem.vue";

let nextTodoId = 0;

export default {
  name: "TodoList",
  components: {
    TodoListItem
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
  },
  methods: {
    addTodo: function() {
      this.todos.push({
        id: nextTodoId++,
        text: this.newTodoText
      });
      this.newTodoText = "";
    },
    removeTodo: function(id) {
      console.log("flag");
      this.todos = this.todos.filter(todo => {
        return todo.id !== id;
      });
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>