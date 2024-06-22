<script setup lang="ts">
import History from '@/components/History.vue'

const model = defineModel()

function handleClickDelete() {
  model.value = ''
}

function handleSearch() {
  if (!model.value) {
    return
  }

  const oldHistory = JSON.parse(sessionStorage.getItem('history')) || []

  if (!oldHistory.includes(model.value)) {
    const newHistory = [model.value, ...oldHistory].slice(0, 20) // ограничение на хранение истории поиска
    window.sessionStorage.setItem('history', JSON.stringify([...newHistory]))
  }

  model.value = ''
}
</script>

<template>
  <div class="search">
    <button @click="handleSearch" class="search__buttonIcon">
      <img src="@/assets/images/search.svg" alt="search-glass" />
    </button>
    <input
      type="text"
      class="search__input"
      v-model="model"
      @keydown.enter.exact="handleSearch"
      placeholder="Поиск фильмов по жанрам и актерам"
    />
    <button v-show="model" @click="handleClickDelete" class="search__buttonIcon">
      <svg
        class="search__buttonIcon__delete"
        width="48"
        height="48"
        viewBox="0 0 48 48"
        fill="currentColor"
        stroke-opacity="0.4"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M10.7573 10.7573L24 24M24 24L37.2426 37.2426M24 24L37.2426 10.7573M24 24L10.7573 37.2426"
          stroke="white"
          stroke-width="4"
          stroke-linecap="round"
          stroke-linejoin="round"
        />
      </svg>
    </button>
  </div>

  <History />
</template>

<style scoped>
.search {
  display: flex;
  gap: 13px;
  padding: 18px 71px;
  border-bottom: 2px solid #fff;
  width: 628px;
  box-sizing: border-box;
  margin: 0 auto;
  align-items: center;
}

.search__input {
  background-color: transparent;
  color: rgba(255, 255, 255, 0.4);
  border: none;
  outline: none;
  font-size: 24px;
  line-height: 36px;
  width: 100%;
}

.search__input:focus {
  color: #fff;
}

.search__buttonIcon {
  background-color: transparent;
  padding: 0;
  border: none;
  cursor: pointer;
  height: 48px;
}

.search__buttonIcon__delete:hover {
  stroke-opacity: 1;
}
</style>
