<script setup>
const name = 'This A Composition Component'

const showName = () => console.log(name)

const id = '1'
const titleClass = 'text-2xl font-bold'

const isLoading = true

const styleButton = {
  disabled: isLoading
}

const getLoadingMessage = () => {
  if (isLoading) {
    return 'Loading....'
  } else {
    return 'Submit'
  }
}
</script>

<template>
  <h1 :id="id" :class="titleClass">{{ name }}</h1>
  <button @click="showName">Composition Component</button>
  <br></br>
  <button v-bind="styleButton">{{ getLoadingMessage() }}</button>
</template>
