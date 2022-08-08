<template>

  <h1>CountIndex {{obj.count}}</h1>

  <CountDisplay v-bind:num="obj.count"></CountDisplay>
  <CountButtons @check="change"></CountButtons>

</template>

<script setup>
import CountDisplay from "@/components/count/CountDisplay";
import CountButtons from "@/components/count/CountButtons";
import {ref} from "vue";

const obj = ref({count:10})

const change = (amount) => {
    console.log(amount)
    obj.value.count += amount
}

</script>

<style scoped>

</style>