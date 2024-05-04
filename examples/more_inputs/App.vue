<script setup lang="ts">
import Child from './Child.vue';
import { ref } from 'vue';

const title = ref<string>('');
const description = ref<string>('')
</script>

<template>
    <h1>title: {{ title }}</h1>
    <h2>description: {{ description }}</h2>
    <Child v-model:title="title" v-model:description="description" />
</template>
