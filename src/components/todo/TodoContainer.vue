<template>
<div class="container">
  <h1>Todo Container {{ref1.refresh}}</h1>
  <TodoInput @changeRefresh="changeRefresh" ></TodoInput>
  <TodoList v-bind:refresh="ref1.refresh"></TodoList>
</div>
</template>

<script setup>

import TodoInput from "@/components/todo/TodoInput";
import TodoList from "@/components/todo/TodoList";
import {ref} from "vue";

const ref1 = ref({refresh:false})

const changeRefresh = () => {
  console.log("change refresh ", ref1.value)
  ref1.value.refresh = !ref1.value.refresh

}

</script>

<style scoped>

</style>