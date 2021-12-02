<template>
  <div class="container">
    <h2 class="title">Poetry is an echo, asking a shadow to dance.
</h2>
    <Poetry />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import Poetry from './components/Poetry.vue'

export default defineComponent({
  name: 'App',
  components: {
    Poetry
  }
})
</script>


