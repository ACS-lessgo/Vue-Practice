<template>
    <h1>Hello template</h1>
    <p>{{ 'Math exp: '+(4+3) }}</p>
    <p>{{ false ? 'Real':'Fake' }}</p>
    <p>{{ getDate() }}</p>
</template>

<script setup>
const getDate = () => {return new Date().toDateString()};
</script>

<style scoped>
h1{
    color: red;
}
</style>