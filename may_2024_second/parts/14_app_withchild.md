# App.vue

```vue {*|2|3|5|9}
<script setup lang="ts">
import Child from './Child1.vue';
import { ref } from 'vue';

const msg = ref<string>('Hello!')
</script>

<template>
  <Child v-model="msg" />
</template>
```
