<script setup>
import { reactive } from 'vue'

const state = reactive({
  name: '',
  check: [],
})
</script>

<template>
  <p>{{ state.name }}</p>
  <p style="white-space: pre-line">{{ state.name }}</p>
  <textarea v-model="state.name" placeholder="add multiple lines" />
  <br />
  <p>Checkbox is {{ state.check }}</p>
  <input type="checkbox" id="jack" value="Jack" v-model="state.check" />
  <label for="jack">Jack</label>
  <input type="checkbox" id="john" value="John" v-model="state.check" />
  <label for="john">John</label>
  <input type="checkbox" id="mike" value="Mike" v-model="state.check" />
  <label for="mike">Mike</label>
</template>
