<script setup lang="ts">
import { ref, watch } from 'vue'

// const movies = ref()
// const test = 'test'
//
// watch(test, () => {})
</script>

<template>
  <div class="block"></div>
</template>

<style scoped>
.block {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
</style>
