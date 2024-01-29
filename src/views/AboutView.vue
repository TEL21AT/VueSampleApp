<script setup>
import HelloWorld from '@/components/HelloWorld.vue'
</script>
<template>
  <div class="about">
    <h1>This is an about page</h1>
    <p>more content here ....</p>

    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App inside AboutView" />
    <HelloWorld msg="another hello world" />
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
