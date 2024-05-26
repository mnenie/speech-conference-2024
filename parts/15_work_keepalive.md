# Работа с KeepAlive

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

```vue{*|5}
// Auth.vue
// если Auth.vue на 2 роута => (/login, /registration)

<template>
  <KeepAlive>
    <AuthForm />
  </KeepAlive>
</template>
```