<template>
  <TodoIndex></TodoIndex>
  <CounterIndex></CounterIndex>
  <hr/>
  <MyHello></MyHello>
  <SayHello userName="Queen" @onName="showName"></SayHello>
</template>

<script>
import MyHello from "@/components/MyHello";
import SayHello from "@/components/SayHello";
import CounterIndex from "@/components/count/CounterIndex";
import TodoIndex from "@/components/todo/TodoIndex";

export default {
  name: 'App',
  components: {
    TodoIndex,
    CounterIndex,
    SayHello,
    MyHello
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
