<template>
  <h1>{{ msg }}</h1>
  <button @click="increment()">count is: {{ count }}</button>
  <p>Edit <code>components/HelloWorld.vue</code> to test hot module replacement.</p>
</template>

<script>

import { defineComponent, ref } from 'vue'

export default defineComponent({
  props: {
    msg: String
  },
  setup() {
    const count = ref(0);
    const increment = () => {
      count.value++;
    }
    return {
      count, increment
    }
  }
})
</script>
