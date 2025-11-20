<script setup>
import { reactive } from 'vue'

const author = reactive({
  name: 'Rendy',
  books: ['Vue.js Basics', 'Advanced Vue.js'],
})

const handleAddBook = () => {
  author.books.push('Vue.js ' + Math.random().toString(2).substring(2))
}

const handleDeleteBook = () => {
  author.books.pop()
}
</script>

<template>
  <h1>
    {{ author.name }}
    <span v-if="author.books.length >= 2"> Have A More Books</span>
    <span v-else-if="author.books.length === 1"> Have A One Books</span>
    <span v-else> Have A Zero Books</span>
  </h1>
  <h1>Total Books : {{ author.books.length }}</h1>
  <button @click="handleAddBook">ADD BOOK</button>
  <button @click="handleDeleteBook">DELETE BOOK</button>
</template>
