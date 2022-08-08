<template>

  <button @click="() => sendClick(1)">INC</button>
  <button @click="() => sendClick(-1)">DEC</button>

</template>

<script setup>

import {defineEmits} from "vue";

const emit = defineEmits(['check'])


const sendClick = (num) => {
  emit('check', num)
}

</script>

<style scoped>

</style>