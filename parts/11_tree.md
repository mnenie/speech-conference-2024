# Жизненный цикл кэшированного компонента

<v-clicks>

<ul class="mb-8">
  <li>onActivated / activated</li>
  <li> onDeactivated / deactivated</li>
</ul>

```vue
<script setup lang="ts">
import { onActivated, onDeactivated } from 'vue'

onActivated(() => {
  // вызывается при первоначальном монтировании
  // и каждый раз, когда он повторно вставляется из кэша
})

onDeactivated(() => {
  // вызывается, когда удаляется из DOM в кэш
  // и также при размонтировании
})
</script>

```

</v-clicks>