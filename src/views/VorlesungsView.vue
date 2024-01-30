<script setup>
import DynamicComp from '@/components/DynamicComp.vue';
import AttributeBinding from '@/components/AttributeBinding.vue';
import EventListener from '@/components/EventListener.vue';
import FormBindung from '@/components/FormBindung.vue';
import VIF from '@/components/VIF.vue';
import ListElement from '@/components/ListElement.vue';
</script>
<template>
  <div class="about">
    <h1>Vorlesungsinhalt</h1>
    <h2>Dynmic vue:</h2>
    <DynamicComp />

    <h2>Attribute Binding:</h2>
    <AttributeBinding />

    <h2>Event Listener</h2>
    <EventListener />

    <h2>Formbinding</h2>
    <FormBindung />

    <h2>V-IF</h2>
    <VIF />

    <h2>Listen in Vue</h2>
    <ListElement />
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
