<script setup>

import CardStack from './CardStack.vue';

const props = defineProps({
     member:{
      type:Object
     }
  })

</script>

<template>

    <!-- debut card -->

<div class="card">
    <div style=""></div>
    <div class="card-image" :style="{ backgroundImage: 'url(' + member.profilePic + ')' }"></div>
    <div class="card-text">
      <span class="job">{{member.jobTitle}}</span>
      <h2>{{ member.firstName+' '+ member.lastName }}</h2>
      <p>{{member.verbatim}}</p>
    </div>
    <CardStack :stack="member.stack" />
  </div>

</template>

<style scoped>

</style>