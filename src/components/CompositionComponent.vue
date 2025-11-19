<script setup>
const { title, button } = defineProps({
  title: String,
  button: String,
})
</script>

<template>
  <h1>{{ title }}</h1>
  <button>{{ button }}</button>
  <br />
</template>
