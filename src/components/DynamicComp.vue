<script setup>
import { ref, reactive } from 'vue'

// component logic
const message = ref('Hello World!');
const counter = reactive({ count: 0 });
</script>

<template>
  <h1>{{ message }}</h1>
  Counter is {{ counter.count }}
</template>