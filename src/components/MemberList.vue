<template>
    <div v-for="member in memberList" :key="member.name">
      <MemberCard :avatar="member.avatar" :name="member.name" :bio="member.bio" :link="member.link" />
    </div>
</template>

<script setup lang="ts">
import MemberCard from './MemberCard.vue';
import { ref } from 'vue';

const memberList = ref([
  {
    avatar : 'https://avatars.githubusercontent.com/u/161844018?v=4',
    name: 'ABloom',
    bio: 'The Flowers There... Are Always in Full Bloom.',
    link: 'https://github.com/abloom25',
    tag: ['开发'],
  },
  {
    avatar: 'https://avatars.githubusercontent.com/u/100058339?v=4',
    name: 'Sean',
    bio: '',
    link: 'https://github.com/makabaka1880',
    tag: ['开发'],
  },
  {
    avatar: 'https://avatars.githubusercontent.com/u/125888129?v=4',
    name: '东风',
    bio: '喜欢睡觉的马赛克工具人。',
    link: 'https://github.com/WindyDante',
    tag: ['开发'],
  },
  {
    avatar : 'https://avatars.githubusercontent.com/u/100515973?v=4',
    name: 'Minc',
    bio: '你已经很棒了!!',
    link: 'https://github.com/minc-nice-100',
    tag: ['运维'],

  },
  {
    avatar: 'https://www.zhilu.cyou/api/avatar.png',
    name: '纸鹿本鹿',
    bio: '纸鹿至麓不知路，支炉制露不止漉。',
    link: 'https://github.com/L33Z22L11',
    tag: ['审核'],
  }
]);

</script>

<style scoped>
</style>
