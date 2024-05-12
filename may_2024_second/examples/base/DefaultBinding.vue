<script setup lang="ts">
import { ref } from 'vue';

const msg = ref('Привет всем!');
</script>

<template>
  <h1>{{ msg }}</h1>
  <input :value="msg" @input="(e: Event) => (msg = (e.target as HTMLInputElement).value)" />
</template>
