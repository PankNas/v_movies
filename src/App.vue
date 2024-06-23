<script setup lang="ts">
import Logo from '@/components/Logo.vue'
import VFooter from '@/components/VFooter.vue'
import Search from '@/components/Search.vue'
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
@font-face {
  font-weight: 400;
  font-family: Roboto;
  font-style: normal;
  src: url('./assets/fonts/Roboto-Regular.woff') format('woff');
  font-display: swap;
}

@font-face {
  font-weight: 700;
  font-family: Roboto;
  font-style: normal;
  src: url('./assets/fonts/Roboto-Bold.woff') format('woff');
  font-display: swap;
}

* {
  font-family: Roboto, sans-serif;
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
