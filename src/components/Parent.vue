<template>
  <Child @fire="callback"></Child>
</template>

<script lang="ts">

import { defineComponent } from 'vue'
import Child from './Child.vue';

export default defineComponent({
  components: {
    Child
  },
  setup() {
    const callback = () => {
      console.log('on Parent');
    }
    return {
      callback
    }
  }
})
</script>
