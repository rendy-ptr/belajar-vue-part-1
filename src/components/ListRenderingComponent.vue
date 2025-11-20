<script setup>
import { reactive } from 'vue'

const author = reactive({
  name: 'Rendy',
  books: [
    {
      title: 'Vue.js 1',
      year: 2019,
    },
    {
      title: 'Vue.js 2',
      year: 2020,
    },
    {
      title: 'Vue.js 3',
      year: 2021,
    },
  ]
})

const handleAddBook = () => {
  author.books.push({
    title: 'Vue.js ' + (author.books.length + 1),
    year: 2021 + author.books.length,
  })
}

const handleDeleteBook = () => {
  author.books.pop()
}
</script>

<template>
  <h1>
    {{ author.name }}
  </h1>
  <h1>Total Books : {{ author.books.length }}</h1>
  <ul v-for="({ title, year }, index) in author.books" :key="`book-${title}-${index}`">
    <li>{{ title }} - {{ year }}</li>
  </ul>
  <button @click="handleAddBook">ADD BOOK</button>
  <button @click="handleDeleteBook">DELETE BOOK</button>
</template>
