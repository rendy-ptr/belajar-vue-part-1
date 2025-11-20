<script setup>
const { title, button } = defineProps({
  title: String,
  button: String,
})

const handleClick = () => {
  console.log(title)
}
</script>

<template>
  <h1>{{ title }}</h1>
  <button @click="handleClick">{{ button }}</button>
  <br />
</template>
