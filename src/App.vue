<script setup lang="ts">
import Nav from '@/components/Nav.vue'
import Footer from '@/components/Footer.vue'
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <main>
    <header>
      <Nav class="nav-container" />
    </header>
    <div class="main-container">
      <router-view />
    </div>
    <footer>
      <Footer now-year="2025" bg-provider="pixiv" class="footer" />
    </footer>
  </main>
</template>

<style scoped>
main {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
  height: 100dvh;
  width: 100dvw;
  background-image: url('/background/1.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  background-attachment: fixed;
  overflow: hidden;
}

header,
footer {
  width: 100%;
  height: fit-content;
  user-select: none;
}

.nav-container {
  padding: 0.5em 2em;
  background-color: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(4px);
}

.main-container {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: flex-start;
  align-items: flex-start;
  padding: 2em 2em;
  overflow-x: hidden;
}

.footer {
  padding: 0.25em 0.5em;
}

</style>
