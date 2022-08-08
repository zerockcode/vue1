<template>

  <h3>TODO  {{userInfo.mid}}</h3>

  <button @click="changeMid">CHANGE</button>

</template>

<script setup>
import {ref, watch} from "vue";

const userInfo = ref({mid:1})

const changeMid = () => {

  userInfo.value.mid += 1
}

watch(userInfo.value, (newValue, oldValue) => {
  console.log("changed...", newValue, oldValue)
})


</script>

<style scoped>

</style>