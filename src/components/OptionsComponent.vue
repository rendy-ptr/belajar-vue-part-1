<script>
export default {
  data() {
    return {
      name: 'This A Options Component',
    }
  },
  methods: {
    showName() {
      console.log(this.name)
    },
  },
}
</script>

<template>
  <h1>{{ name }}</h1>
  <button @click="showName">Options Component</button>
</template>
