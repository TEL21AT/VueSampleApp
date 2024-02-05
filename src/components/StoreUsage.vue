<template>
    <main>
        <p>Count is: {{ counterStore.count }}</p>
        <button @click="counterStore.increment()">Increment</button>
    </main>
</template>

<script setup>
import { useCounterStore } from '@/stores/counter';

const counterStore = useCounterStore();
</script>