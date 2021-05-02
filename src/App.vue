<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <!-- <HelloWorld msg="Hello Vue 3.0 + Vite" /> -->
  <!-- <Props msg="Props" :callback="callback"></Props> -->
  <Parent />
</template>

<script lang="ts">
import { defineComponent, onMounted, reactive } from 'vue'
import HelloWorld from './components/HelloWorld.vue'
import Props from './components/Props.vue';
import Parent from './components/Parent.vue';

export default defineComponent({
  components: {
    HelloWorld,
    Props,
    Parent
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
