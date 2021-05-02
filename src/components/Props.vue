<template>
  <h1>{{ msg }}</h1>
  <button @click="increment()">count is: {{ count }}</button>
</template>

<script lang="ts">

import { defineComponent, ref, PropType } from 'vue'

export default defineComponent({
  props: {
    msg: String,
    callback: {
      type: Function as PropType<(v: String) => void>,
      required: true
    }
  },
  setup(props) {
    const count = ref(0);
    const increment = () => {
      count.value++;
      props.callback(`*** ${count.value} clicked ***`);
    }
    return {
      count, increment
    }
  }
})
</script>
