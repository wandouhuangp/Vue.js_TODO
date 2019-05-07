<template>
  <div>
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

export default {
  name: "TodoList",
  components: {
    TodoListItem
  },
  props: {
    todos: Array,
    required: true
  },
  methods: {
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