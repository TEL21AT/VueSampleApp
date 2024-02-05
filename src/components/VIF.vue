<script setup>
import { ref } from 'vue'

const awesome = ref(true)

function toggle() {
    awesome.value = !awesome.value
}
</script>

<template>
  <button @click="toggle">toggle</button>
  <h3 v-if="awesome">Vue is awesome!</h3>
  <h3 v-else>Oh no 😢</h3>
</template>