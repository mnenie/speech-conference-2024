<script setup lang="ts">
const title = defineModel<string>('title');
const description = defineModel<string>('description');
</script>

<template>
  <input v-model="title" />
  <input v-model="description" />
</template>
