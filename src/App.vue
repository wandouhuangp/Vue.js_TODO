<template>
  <div id="app">
    <HelloWorld msg="Hello World!">Mark</HelloWorld>
    <div>Some additional content here.</div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",
  components: {
    HelloWorld
  }
};
</script>

<style>
body {
  padding: 50px;
}
</style>
