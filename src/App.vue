<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <!-- <HelloWorld msg="Hello Vue 3.0 + Vite" /> -->
  <Props msg="Props" :callback="callback"></Props>
</template>

<script lang="ts">
import { defineComponent, onMounted, reactive } from 'vue'
import HelloWorld from './components/HelloWorld.vue'
import Props from './components/Props.vue';

export default defineComponent({
  components: {
    HelloWorld,
    Props
  },
  setup() {
    const callback = (v: string) => {
      console.log(v);
    }
    return {
      callback
    }
  }
})
</script>
