<template>
  <div class="member-view">
    <h1>成员</h1>
    <MemberList />
  </div>
</template>

<script setup lang="ts">
import MemberList from '@/components/MemberList.vue';
</script>

<style scoped>
.member-view {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  width: 100%;
  height: 100%;
  gap: 1em;
}
</style>
