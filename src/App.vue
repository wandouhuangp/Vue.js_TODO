<template>
  <div id="app">
    <TodoListItem todo="{text: '1st Todo!'}"></TodoListItem>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import TodoListItem from "./components/TodoListItem";
export default {
  name: "App",
  components: {
    HelloWorld,
    TodoListItem
  }
};
</script>

<style>
body {
  padding: 50px;
}
</style>
