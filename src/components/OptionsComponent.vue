<script>
export default {
  props: {
    title: String,
    button: String,
  },
}
</script>

<template>
  <h1>{{ title }}</h1>
  <button>{{ button }}</button>
</template>
