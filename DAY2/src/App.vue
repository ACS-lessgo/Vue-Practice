<template>
  <div class="main-container">
    <!-- <blog Title="Title 1" Description="Content 1"></blog>
    <blog Title="Title 2" Description="Content 2"></blog>
    <blog Title="Title 3" Description="Content 3"></blog> -->
    <directive></directive>
  </div>
</template>

<script setup>
// import blog from "./components/blog.vue";
import directive from "./components/directive.vue"
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@100&display=swap");

body {
  margin: 0px;
  height: 100vh;
  font-family: "Roboto", sans-serif;
}

#app {
  height: 100%;
}

.main-container {
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
</style>
