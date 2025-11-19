<script setup>
const name = 'This A Composition Component'

const showName = () => console.log(name)
</script>

<template>
  <h1>{{ name }}</h1>
  <button @click="showName">Composition Component</button>
</template>
