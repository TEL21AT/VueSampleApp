<template>
    <h3>My injected value is: {{ messageObject.message }}</h3>
</template>

<script setup>
import { inject } from 'vue';

const messageObject = inject('message');
messageObject.changeMessage('Hello from ProvideInject.vue');

</script>