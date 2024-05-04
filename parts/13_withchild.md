# Child.vue

````md magic-move
```vue {*|3}
<script setup lang="ts">
defineProps<{
  modelValue: string;
>();
</script>

<template>
  <input :value="modelValue" />
</template>

```

```vue {*|2}
<script setup lang="ts">
const emits = defineEmits(["update:modelValue"]);
</script>

<template>
  <input @input="emits('update:modelValue', ($event.target as HTMLInputElement).value)" />
</template>
```

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
````
