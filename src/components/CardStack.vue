<script setup>
//defineprops est automatiquement importé
//import { defineProps } from 'vue';

//import {computed} from 'vue';

const props = defineProps({
  stack: {
    type: Array,
   // default: () => [],
  },
});

const showPizzas = (level) => '🍕'.repeat(level);
//const showPizzas = computed(() => { return '🍕'.repeat(stack.level) } );
const showBroccolis = (broccoli) => '🥦'.repeat(broccoli);
const showSteaks = (steak) => '🥩'.repeat(steak);

</script>

<template>
  <div class="card-stats">
    <div v-for="item in stack" :key="item.label" class="stat">
      <div class="techno">{{ item.label }}</div>
      <div class="level">{{showPizzas(item.level) /* showPizzas */|| showBroccolis(item.broccoli) || showSteaks(item.steak)}}</div>
    </div>
  </div>
</template>

<style scoped>


</style>

