<template>
  <div class="project-view">
    <h1>项目列表</h1>
    <ProjectList />
  </div>
</template>

<script setup lang="ts">
import ProjectList from "@/components/ProjectList.vue";
</script>

<style scoped>
.project-view {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  width: 100%;
  height: 100%;
  gap: 1em;
}
</style>
