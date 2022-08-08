<template>
<h2 @click="clickName" >{{props.userName}}</h2>
</template>

<script setup>
import { defineProps } from "vue";
import { defineEmits } from 'vue'
const emit = defineEmits(['onName'])

const props = defineProps({
  userName:String,
  fn:Function
})

const clickName = () => {
  alert("NameClick")
  emit('onName', 'AAAAAAAAAAAAAAAAAAAAAAA')
}

</script>

<style scoped>

</style>