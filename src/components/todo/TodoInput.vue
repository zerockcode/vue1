<template>
<div>
  <h1>Todo Input Div</h1>
  <p>
    <input type="text" v-model="todo.title">
  </p>
  <p>
    <input type="date" v-model="todo.dueDate">
  </p>
  <p>
    <button @click="addServer">ADD</button>
  </p>
</div>
</template>

<script setup>

import {ref, defineEmits} from "vue";
import axios from "axios";

const emit = defineEmits(['changeRefresh'])

const todo = ref({title:'AAA',dueDate:'2022-10-10',complete:false})

const addServer = async () => {

  console.log(todo.value)

  axios.post('http://localhost/todos/',todo.value).then(res => {
    console.log(res)
    emit('changeRefresh')
  })

}


</script>

<style scoped>

</style>