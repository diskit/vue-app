<template>
  <Event @fire="callback"></Event>
</template>

<script lang="ts">

import { defineComponent } from 'vue'
import Event from './Event.vue'

export default defineComponent({
  components: {
    Event
  },
  setup() {
    const callback = (value) => {
      console.log('on Child', value)
    }
    return {
      callback
    }
  }
})
</script>
