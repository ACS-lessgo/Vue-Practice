<template>
  <h1>Count : {{ count }}</h1>
  <button @click="increment">Click</button>
</template>

<script setup>
import { reactive ,ref} from "vue";
//const state = reactive({ count: 0 });
const count = ref(0)
const increment = () => {
  //return state.count++;
  return count.value++;
};
</script>
