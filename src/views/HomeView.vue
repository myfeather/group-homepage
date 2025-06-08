<script setup lang="ts">
import Button from '@/components/Button.vue';
import { RouterLink } from 'vue-router';
</script>

<template>
<div class="home-view">
  <h1>FeatherDev</h1>
  <h2>片羽开发组</h2>
  <p>我们坚信，美好的科技会为人们带来曙光。</p>
  <div class="button-container">
    <RouterLink to="/project">
      <Button>项目</Button>
    </RouterLink>
    <RouterLink to="/member">
      <!-- <Button>成员</Button> -->
    </RouterLink>
  </div>
</div>
</template>

<style scoped>
.home-view {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  width: 100%;
  height: 100%;
  gap: 1em;
}
.button-container {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
  gap: 1em;
}
</style>
