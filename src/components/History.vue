<script setup lang="ts">
type Props = {
  history: string[]
}

defineProps<Props>()
defineEmits(['clickHistoryItem'])
</script>

<template>
  <ul class="list">
    <li v-for="(item, index) in history" :key="item">
      <button class="list__item" @click="$emit('clickHistoryItem', index)">{{ item }}</button>
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
  border: none;
  cursor: pointer;
}

.list__item:hover {
  background-color: #ffffff;
}
</style>
