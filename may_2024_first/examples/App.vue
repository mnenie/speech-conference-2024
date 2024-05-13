<template>
  <RouterView v-slot="{ Component }">
    <KeepAlive :include="['Login', 'Registration']">
      <component :is="Component" />
    </KeepAlive>
  </RouterView>
</template>