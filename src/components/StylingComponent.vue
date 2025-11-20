<script setup>
import { reactive } from 'vue'

const state = reactive({
  number: 0,
  color: 'black',
  align: 'center',
  font: '48px',
})

const buttons = [
  {
    label: 'Green',
    color: 'green',
  },
  {
    label: 'Blue',
    color: 'blue',
  },
  {
    label: 'Red',
    color: 'red',
  },
  {
    label: 'Yellow',
    color: 'yellow',
  },
  {
    label: 'Lilac',
    color: '#C8A2C8',
  },
  {
    label: 'Reset',
    color: 'black',
  }
]

const actionButton = [
  {
    label: 'Increment',
    backgroundColor: 'cyan',
    operation: () => {
      state.number++
    },
  },
  {
    label: 'Decrement',
    backgroundColor: 'salmon',
    operation: () => {
      state.number--
    },
  },
]

const baseStyle = {
  color: 'white',
  border: 'none',
  padding: '8px 16px',
  borderRadius: '5px',
  cursor: 'pointer',
  boxShadow: '0 4px 6px rgba(0, 0, 0, 0.1)',
}

const setColor = (color) => {
  state.color = color
}
</script>

<template>
  <h1 class="text-center" :style="{ color: state.color, textAlign: state.align, fontSize: state.font }">
    {{ state.number }}
  </h1>
  <div class="button-parent">
    <button
      v-for="{ label, color } in buttons"
      :key="label"
      :style="{
        ...baseStyle,
        backgroundColor: color,
      }"
      @click="setColor(color)"
    >
      {{ label }}
    </button>
  </div>
  <div class="button-parent">
    <button
      v-for="{ label, operation, backgroundColor } in actionButton"
      :key="label"
      :style="{
        ...baseStyle,
        backgroundColor,
      }"
      @click="operation()"
    >
      {{ label }}
    </button>
  </div>
</template>

<style scoped>

.button-parent {
  display: flex;
  justify-content: center;
  gap: 12px;
  margin-top: 16px;
}
</style>
