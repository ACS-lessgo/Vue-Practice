<template>
    <div class="main-container">
        <h1>Hello Vue</h1>
        <!-- <Button></Button> -->
        <Template></Template>
        <Counter></Counter>
    </div>
</template>

<script setup>
//import Button from "./components/Button.vue"
//import Template from "./components/Template.vue"
import Counter from "./components/Counter.vue"
</script>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100&display=swap');

    body {
        margin: 0px;
        height: 100vh;
        font-family: 'Roboto', sans-serif;
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
