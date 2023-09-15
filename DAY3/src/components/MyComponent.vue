<template>
  <h1>My Component</h1>
  <button @click="btnClick">Click me</button>
</template>

<script setup>
import {ref} from 'vue'
const emits = defineEmits(['on-btn-click'])
const btnClick = ()=> {emits('on-btn-click',count.value)}
const count = ref(10)
</script>
