<template>
  <div>
    <h1>COUNT VALUE</h1>
    <h2> {{num}}</h2>
  </div>
</template>

<script setup>
import {defineProps} from "vue";

const props = defineProps({num:Number})

console.log(props)


</script>

<style scoped>

</style>