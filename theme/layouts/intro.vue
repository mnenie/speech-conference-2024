<script setup lang="ts">
defineProps<{
  author: string,
  name: string,
  telegram?: string,
  github?: string,
}>()
</script>
<template>
  <div class="slidev-layout flex flex-col justify-center items-center">
    <span text-5xl>{{ name }}</span>
    <span text-3xl pt6>{{ author }}</span>

    <div  absolute pos="bottom-xl right-xl" flex="~ col">
      <div v-if="telegram">
        {{ telegram }}
      </div>
      <div v-if="github">
        {{ github }}
      </div>
    </div>
  </div>
</template>