<template>
    <h3>My Prop value is: {{ props.exampleProp }}</h3>
    <button @click="emit('exampleEvent', 'exampleArgument')">Emit Event!</button>
</template>

<script setup>
const props = defineProps(['exampleProp']);
const emit = defineEmits(['exampleEvent'])
</script>