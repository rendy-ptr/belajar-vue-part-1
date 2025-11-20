<script setup>
import { reactive, ref, computed } from 'vue'

const author = reactive({
  name: 'Rendy',
  books: ['Vue.js Basics', 'Advanced Vue.js'],
})

const isPublished = computed(() => {
  console.log(author.books)
  return author.books.length > 0 ? 'Published Yes' : 'Published No'
})

const count = ref(0)

const handleIncrement = () => {
  count.value++
}

const handleAddBook = () => {
  author.books.push('Vue.js ' + count.value)
}

const handleDeleteBook = () => {
  author.books.pop()
}
</script>

<template>
  <h1>{{ isPublished }}</h1>
  <p>{{ count }}</p>
  <button @click="handleIncrement">+</button>
  <button @click="handleAddBook">ADD BOOK</button>
  <button @click="handleDeleteBook">DELETE BOOK</button>
</template>
