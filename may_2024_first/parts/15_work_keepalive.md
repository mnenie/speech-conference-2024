# Работа с KeepAlive

<v-clicks>

```vue{*|5}
// app.vue

<template>
  <RouterView v-slot="{ Component }">
    <KeepAlive :include="['Login', 'Registration']">
      <component :is="Component" />
    </KeepAlive>
  </RouterView>
</template>
```

если Auth.vue на 2 роута => (/login, /registration)

```vue{*|5}
// Auth.vue

<template>
  <KeepAlive>
    <AuthForm />
  </KeepAlive>
</template>
```

</v-clicks>
