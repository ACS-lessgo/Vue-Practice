<template>
  <div class="blogCard">
    <h1>Blog</h1>
    <h3>{{ Title }}</h3>
    <p>{{ Description }}</p>
  </div>
</template>

<script setup>
defineProps({
  Title: { type: String, required: true },
  Description: { type: String, required: true },
});
</script>

<style scoped>
.blogCard {
  border: 1px solid black;
  padding: 15px;
}
</style>
