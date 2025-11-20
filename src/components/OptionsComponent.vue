<script>
export default {
  props: {
    title: String,
    button: String,
  },
  methods: {
    handleClick() {
      console.log(this.title)
    },
  },
}
</script>

<template>
  <h1>{{ title }}</h1>
  <button @click="handleClick">{{ button }}</button>
</template>
