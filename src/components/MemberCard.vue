<template>
  <div class="member-card" @click="openLink">
    <img v-if="props.avatar" :src="props.avatar" :alt="props.name + '的头像'" draggable="false"/>
    <div class="member-info">
      <h3>{{ props.name }}</h3>
      <p>{{ props.bio }}</p>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue';

const props = defineProps<{
  avatar: string;
  name: string;
  bio: string;
  link: string;
}>();

function openLink() {
  window.open(props.link, '_blank');
}

</script>

<style scoped>
.member-card {
  display: flex;
  flex-direction: flex-end;
  justify-content: flex-start;
  align-items: center;
  border-radius: 2em;
  padding: 1em;
  width: 100%;
  max-width: 40em;
  height: fit-content;
  transition: all 0.3s ease-in-out;
  gap: .5em;
  cursor: pointer;
  box-shadow: 0 0 15px rgba(255, 255, 255, 0);
  border: 1px solid rgba(255, 255, 255, 0);

}

.member-card img {
  width: 5em;
  height: 5em;
  border-radius: 1em;
}

.member-card:hover {
  box-shadow: 0 0 15px rgba(255, 255, 255, 0.2);
  backdrop-filter: blur(2px);
  border: 1px solid rgba(255, 255, 255, 0.1);
  background-color: rgba(255, 255, 255, 0.1);
}
</style>
