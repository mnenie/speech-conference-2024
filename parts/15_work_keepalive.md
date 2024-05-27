# Работа с KeepAlive

<div>
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
</div>

<div v-click>
```vue
// Auth.vue
// если Auth.vue на 2 роута => (/login, /registration)

<template>
  <KeepAlive>
    <AuthForm />
  </KeepAlive>
</template>
```
</div>
