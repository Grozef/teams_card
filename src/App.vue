<script setup>

import {ref} from 'vue';
import IdCard from './components/IdCard.vue';
import {TEAMS} from './assets/teamsApp';

const teamList = ref(TEAMS);

</script>

<template>

<body>
  
  <IdCard  v-for="member in teamList"
          :key="member.profilePic"
          :member="member"
  />


</body>

</template>

<style scoped>

</style>
