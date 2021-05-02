<template>
  <button @click="onClick()">Click me</button>
</template>

<script lang="ts">

import { defineComponent } from 'vue'

export default defineComponent({
  setup(_, context) {
    
    const onClick = () => {
      context.emit('fire', {message: 'clicked'})
    }
    return {
      onClick
    }
  }
})
</script>
