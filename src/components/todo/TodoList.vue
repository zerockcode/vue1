<template>
<h1>Todo List Div</h1>
<h2>REFRESH {{props.refresh}}</h2>
<ul>
  <li v-for="todo in state.list"  :key="todo.id">
    {{todo.id}} --- {{todo.title}}
  </li>
</ul>
</template>

<script setup>
import {defineProps, onMounted, ref, watch} from "vue";
import axios from "axios";

console.log("Todo List.............")

const props = defineProps({refresh:Boolean})

const state = ref({list:[]})

const getServerList = async () => {
  axios.get("http://localhost/todos").then(res => {
    const data = res.data
    console.log(data)
    state.value.list = data
  })
}

watch(props,() => {
  console.log("refreh... Todo List")
  getServerList()
})

onMounted(() => {
  getServerList()
})

</script>

<style scoped>

</style>