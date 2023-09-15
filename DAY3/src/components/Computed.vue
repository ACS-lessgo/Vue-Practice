<template>
  <h1>Computed Properties</h1>
  <h1>Age : {{ age }}</h1>
  <h1>A : {{ a }}</h1>
  <h1>B : {{ b }}</h1>
  <h1>Age + A : {{ sumAgeA }}</h1>
  <h1>Age + B : {{ sumAgeB }}</h1>
  <button @click="addToA">Add to A</button>
  <button @click="addToB">Add to B</button>
</template>

<script setup>
import {ref,computed} from 'vue'

const a = ref(0)
const b = ref(0)
const age = ref(20)

const addToA = () => {a.value++}
const addToB = () => {b.value++}
const sumAgeA = computed(() => {console.log('sumAgeA called');return age.value+a.value})
const sumAgeB = computed(() => {console.log('sumAgeB called');return age.value+b.value})

</script>