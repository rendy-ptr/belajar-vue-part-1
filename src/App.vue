<script setup>
import CompositionComponent from './components/CompositionComponent.vue'
import ComputedComponent from './components/ComputedComponent.vue'
import OptionsComponent from './components/OptionsComponent.vue'
import ReactiveComponent from './components/ReactiveComponent.vue'
</script>

<template>
  <OptionsComponent :title="`Ini Options Component`" :button="`Button Options Component`" />
  <hr />
  <CompositionComponent
    :title="`Ini Composition Component`"
    :button="`Button Composition Component`"
  />
  <hr />
  <ReactiveComponent :title="`Ini Reactive Component`" />
  <hr />
  <ComputedComponent />
</template>

<style scoped></style>
