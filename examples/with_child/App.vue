<script setup lang="ts">
import Child from './Child1.vue';
import { ref } from 'vue';

const msg = ref<string>('Hello!')
</script>

<template>
  <Child v-model="msg" />
</template>
