# Рассмотрим базовые примеры

Посмотрите на реализацию!

````md magic-move
```vue
<script setup lang="ts">
import { ref } from 'vue';

const msg = ref('Привет всем!');
</script>

<template>
  <h1>{{ msg }}</h1>
  <input :value="msg" @input="(e) => (msg = (e.target as HTMLInputElement).value)" />
</template>

```
```vue{*|13}
<script setup lang="ts">
import { ref } from 'vue';

const msg = ref('Привет всем!');
</script>

<template>
  <h1>{{ msg }}</h1>
  <input v-model="msg" />
</template>


// Проще не правда ли?
```
````
