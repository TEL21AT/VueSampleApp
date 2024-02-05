<template>
    <h3>My injected value is: {{ message }}</h3>
</template>

<script setup>
import { inject } from 'vue';

const message = inject('message');
</script>