<script setup>
import { ref, reactive } from 'vue'
import { useCounterStore } from '@/stores/counter';

// component logic
const message = ref('Hello World!');
const counter = reactive({ count: 0 });
setInterval(() => {
  counter.count++;
}, 2000);
const counterStore = useCounterStore();
</script>

<template>
  <h3>{{ message }}</h3>
  Counter is {{ counter.count }}<br />
  Counter in store is {{ counterStore.count }}
</template>