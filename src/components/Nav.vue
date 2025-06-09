<script setup lang="ts">
import { ref } from 'vue';
import { RouterLink} from 'vue-router'

const navItems = ref([
  { name: '主页', path: '/' },
  { name: '项目', path: '/project' },
  { name: '成员', path: '/member' },

]);

  // { name: '关于', path: '/about' },
</script>

<template>
  <div class="wrapper">
      <RouterLink to="/"><h1>FeatherDev</h1></RouterLink>
    <nav>
      <div v-for="item in navItems" :key="item.name" class="nav-item">
        <RouterLink :to="item.path">{{ item.name }}</RouterLink>
      </div>
    </nav>
  </div>
</template>

<style scoped>
.wrapper {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  height: fit-content;
  color: rgb(255, 255, 255);
}

nav {
  width: fit-content;
  display: flex;
  justify-content: flex-end;
  align-items: center;
}

.nav-item * {
  border: 1px solid rgba(255, 255, 255, 0);
  transition: all 0.3s ease-in-out;
  padding: .25em .5em;
  border-radius: 1em;
}

.nav-item :hover {
  backdrop-filter: blur(2px);
  /* padding: 0.5em 1em; */
  box-shadow: 0 0 10px rgba(255, 255, 255, 0.1);
  border: 1px solid rgba(255, 255, 255, 0.1);
  background-color: rgba(255, 255, 255, 0.1);
}

h1 {
  font-size: 1em;
}
</style>
