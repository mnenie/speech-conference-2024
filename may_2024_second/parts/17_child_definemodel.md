<h1>Структура <span v-mark.circle>Child.vue</span></h1>

<v-clicks>

#### c

````md magic-move
```vue
defineProps<{
  modelValue: string;
>();
const emits = defineEmits(["update:modelValue"]);

```
````

#### на

```vue
const model = defineModel<string>()
```

#### получаем

```vue
<script setup lang="ts">
const model = defineModel<string>();
</script>

<template>
  <input v-model="model" />
</template>

```
</v-clicks>
