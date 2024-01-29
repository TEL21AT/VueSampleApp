<script setup>
import DynamicComp from '@/components/DynamicComp.vue';
import AttributeBinding from '@/components/AttributeBinding.vue';
</script>
<template>
  <div class="about">
    <h1>Vorlesungsinhalt</h1>
    <h2>Dynmic vue:</h2>
    <DynamicComp />

    <h2>Attribute Binding:</h2>
    <AttributeBinding />
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
