#### Child.vue

```vue {*|2|3|7|8|*}
<script setup lang="ts">
const title = defineModel<string>('title');
const description = defineModel<string>('description');
</script>

<template>
  <input v-model="title" />
  <input v-model="description" />
</template>
```

#### App.vue

```vue {*|5|6|10|11|12}
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
```
