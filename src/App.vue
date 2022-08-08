<template>
  <TodoContainer></TodoContainer>
</template>

<script>

import TodoContainer from "@/components/todo/TodoContainer";

export default {
  name: 'App',
  components: {
    TodoContainer
  },
  methods: {
    showName: (value) => {
      alert("AAAA" + value)
    }
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
  margin-top: 60px;
}
</style>
