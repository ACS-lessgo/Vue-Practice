<template>
  <h1>Directive</h1>
  <!-- v-bind -->
  <a :href="url">Figma</a>
  <!-- v-html -->
  <span v-html="rawHtml"></span>
  <!-- v-for -->
  <ul>
    <li v-for="(item, index) in items" :key="index">
      {{ item.id + " " + item.name }}
    </li>
  </ul>
  <!-- v-model -->
  <h1>{{ message }}</h1>
  <input type="text" v-model="message" placeholder="enter text" />

  <h1>{{ count }}</h1>
  <button @click="increment">Add</button>
  <button @dblclick="increment">Double Click to add</button>
  <button @click.once="increment">Add Once</button>

  <h1 v-if="showGreeting">Hello there</h1>
  <button @click="showText">{{ buttonMessage }}</button>
</template>

<script setup>
import { ref } from "vue";
const url = ref(
  "https://www.figma.com/file/ne9I7ZWuxSMbdC4ni3EclH/DsTube?type=design&node-id=0-1&mode=design&t=kTL8FP3RU900rng8-0"
);
const rawHtml = ref('<span style="color:red">This should be ignored</span>');
const items = ref([
  { id: 1, name: "Abc" },
  { id: 2, name: "Def" },
  { id: 3, name: "Ghi" },
]);
const message = ref("");
const count = ref(0);
const increment = () => {
  count.value++;
};
const showGreeting = ref(false);
const showText = () => {
  showGreeting.value = !showGreeting.value;
  if (showGreeting.value == true) {
    buttonMessage.value = "Hide Text";
  } else {
    buttonMessage.value = "Show Hidden Text";
  }
};
const buttonMessage = ref("Show Hidden Text");
</script>

<style></style>
