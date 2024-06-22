<script setup lang="ts">
import Logo from '@/components/Logo.vue'
import Search from '@/components/Search.vue'
import VFooter from '@/components/VFooter.vue'
</script>

<template>
  <body class="body">
    <main class="main">
      <Logo />
      <Search />
    </main>
    <VFooter />
  </body>
</template>

<style>
* {
  margin: 0;
  box-sizing: border-box;
}

.body {
  background-color: #1c1c1c;
  width: 100%;
  height: 100%;
  padding: 80px 0 16px;
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.main {
  display: flex;
  flex-direction: column;
  flex: 1;
  margin: 0 auto;
  width: 1210px;
  gap: 54px;
}
</style>
