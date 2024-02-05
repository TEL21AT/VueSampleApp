<script setup>
import { ref } from 'vue'

const titleClass = ref('title')
</script>

<template>
  <h3 v-bind:class="titleClass">Make me red</h3> <!-- add dynamic class binding here -->
</template>

<style>
.title {
  color: red;
}
</style>