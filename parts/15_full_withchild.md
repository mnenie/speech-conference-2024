# Сhild.vue + App.vue

```vue
<script setup lang="ts">
defineProps<{
  modelValue: string;
>();
const emits = defineEmits(["update:modelValue"]);
</script>

<template>
  <input :value="modelValue" @input="emits('update:modelValue', ($event.target as HTMLInputElement).value)" />
</template>
```


```vue
<script setup lang="ts">
import Child from './Child1.vue';
import { ref } from 'vue';

const msg = ref<string>('Hello!')
</script>

<template>
  <Child v-model="msg" />
</template>
```
