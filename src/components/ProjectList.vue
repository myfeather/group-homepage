<template>
  <div v-for="project in projectList" :key="project.title">
      <ProjectCard :icon="project.icon" :title="project.title" :description="project.description" :link="project.link" />
  </div>
</template>

<script setup lang="ts">
import ProjectCard from '@/components/ProjectCard.vue';
import { ref } from 'vue';

const projectList = ref([
  {
    icon : 'https://afeather.cn/favicon.ico',
    title: 'A Feather | 一片羽',
    description: '让零散的心事落地成光。',
    link: 'https://afeather.cn',
  },
  {
    icon : '/Lexicalis.svg',
    title: 'Lexicalis | 辞点',
    description: '与@PromptCraft共同开发。一个基于BERT与DeepSeek的词典。',
    link: 'https://lexicalis.xyz',
  },
  {
    icon : '/Gloweve.svg',
    title: 'Gloweve | 辉夜',
    description: 'A Feather 所使用的设计语言的配套主题Api。',
    link: 'https://gloweve.com',
  },
]);

</script>

<style scoped>
</style>
