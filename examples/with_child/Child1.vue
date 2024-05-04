<script setup lang="ts">
defineProps<{
  modelValue: string;
}>();

const emits = defineEmits(["update:modelValue"]);
</script>

<template>
  <input :value="modelValue" @input="emits('update:modelValue', ($event.target as HTMLInputElement).value)" />
</template>
