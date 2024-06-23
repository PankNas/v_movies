<script setup lang="ts">
type Props = {
  history: string[]
}

defineProps<Props>()
</script>

<template>
  <ul class="list">
    <li v-for="item in history" :key="item" class="list__item">
      {{ item }}
    </li>
  </ul>
</template>

<style scoped>
.list {
  display: flex;
  gap: 8px;
  list-style: none;
  padding: 0;
  flex-wrap: wrap;
}

.list__item {
  background-color: rgba(255, 255, 255, 0.8);
  padding: 6px 16px;
  border-radius: 4px;
}
</style>
