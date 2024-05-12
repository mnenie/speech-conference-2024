
# Разберемся подробнее

<span v-mark.orange>Общие части</span>

<v-clicks>

````md magic-move
```vue{2}
<script setup lang="ts">
import { ref } from 'vue';
```
```vue{4}
<script setup lang="ts">
import { ref } from 'vue';

const msg = ref('Привет всем!');
</script>
```

```vue{8}
<script setup lang="ts">
import { ref } from 'vue';

const msg = ref('Привет всем!');
</script>

<template>
  <h1>{{ msg }}</h1>
```

```vue{9}
<script setup lang="ts">
import { ref } from 'vue';

const msg = ref('Привет всем!');
</script>

<template>
  <h1>{{ msg }}</h1>
  <input ... />
```
````

<h4 class="absolute bottom-28 right-28">А как произвести то самое <span v-mark="{ at: 7, color: '#234', type: 'circle' }">двустороннее связывание </span> во Vue?</h4>

</v-clicks>