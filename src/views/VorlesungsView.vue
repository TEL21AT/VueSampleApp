<script setup>
import DynamicComp from '@/components/DynamicComp.vue'
import AttributeBinding from '@/components/AttributeBinding.vue'
import EventListener from '@/components/EventListener.vue'
import FormBindung from '@/components/FormBindung.vue'
import VIF from '@/components/VIF.vue'
import ListElement from '@/components/ListElement.vue'
import PropsAndEvents from '@/components/PropsAndEvents.vue'
import ProvideInject from '@/components/ProvideInject.vue'
import StoreUsage from '@/components/StoreUsage.vue'
import { provide } from 'vue'
import { reactive } from 'vue'
const messageObject = reactive({
  message: 'Hello World!',
  changeMessage: (value) => {
    messageObject.message = value
  }
});

provide('message', messageObject)
</script>

<template>
  <div class="about">
    <h1>Vorlesungsinhalt</h1>

    <h2 class="custom-header">Dynamic vue:</h2>
    <DynamicComp />
    <hr />

    <h2 class="custom-header">Attribute Binding:</h2>
    <AttributeBinding />
    <hr />
    <h2 class="custom-header">Event Listener</h2>
    <EventListener />
    <hr />
    <h2 class="custom-header">Formbinding</h2>
    <FormBindung />
    <hr />
    <h2 class="custom-header">V-IF</h2>
    <VIF />
    <hr />
    <h2 class="custom-header">Listen in Vue</h2>
    <ListElement />
    <hr />
    <h2 class="custom-header">Props & Events Demo:</h2>
    <PropsAndEvents
      exampleProp="This is a prop!"
      @exampleEvent="
        (arg) => {
          console.log(arg + ' received!')
        }
      "
    />
    <hr />
    <h2 class="custom-header">Provide & Inject Demo:</h2>
    <ProvideInject />
    <hr />
    <h2 class="custom-header">Pinia Store</h2>
    <StoreUsage />
    <hr />
  </div>
</template>

<style>
.about {
  min-height: 100vh;
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
  text-align: center;
}
hr {
  width: 50%;
  margin: 20px;
}
.custom-header {
  font-size: 20px;
  font-weight: bold;
  margin-bottom: 20px;
  text-decoration: underline;
}
</style>
