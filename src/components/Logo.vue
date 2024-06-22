<script lang="ts">
export default {
  name: "Logo"
}
</script>

<template>
  <div class="logo">
    <img src="@/assets/images/symbol-t.png" alt="" class="image_symbol">
    <span class="wrapper">
      <img src="@/assets/images/play.png" alt="" class="image">
      <img src="@/assets/images/stop.png" alt="" class="image">
    </span>
    <img src="@/assets/images/symbol-p.png" alt="" class="image_symbol">
  </div>
</template>

<style scoped>
.logo {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
}

.image_symbol {
  width: 44px;
}

.image {
  width: 16px;
  height: 24px;
}

.wrapper {
  display: flex;
  align-items: center;
  gap: 3px;
}
</style>