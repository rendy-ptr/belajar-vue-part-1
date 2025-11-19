<script setup>
import { reactive } from 'vue'

const { title } = defineProps({
  title: String,
})

const state = reactive({
  count: 0,
})
</script>

<template>
  <div>
    <h1>{{ title }}</h1>
    <p>{{ state.count }}</p>
    <button @click="state.count++">+</button>
    <button @click="state.count--">-</button>
  </div>
</template>
