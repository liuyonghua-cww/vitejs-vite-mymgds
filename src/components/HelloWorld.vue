<template>
  <span @click="increment">{{ state.number }}</span>
</template>
<script setup lang="ts">
import { ref, reactive, nextTick } from 'vue';

defineProps<{ msg: string }>();

const state = reactive({ number: 1 });
const increment = () => {
  state.number++
};
nextTick(() => {
  console.log('nextTick')
})
</script>

<style scoped></style>
