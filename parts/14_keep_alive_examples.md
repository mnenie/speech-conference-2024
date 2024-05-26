# Разберемся подробнее в решении

<v-clicks>

````md magic-move
```vue
<template>
  <form @submit.prevent="onSubmit">...</form>
</template>
```

```vue{*|7|8}
<template>
  <form @submit.prevent="onSubmit">
    <UiFormField v-slot="{ componentField }" name="email" :validate-on-blur="!isFieldDirty">
      <UiFormItem class="grid justify-items-start gap-2" v-auto-animate>
        <UiLabel for="email"> Email </UiLabel>
          <UiFormControl>
            <UiInput
              v-model="email"
              v-bind="componentField"
              id="email"
              placeholder="user@example.com"
              type="email"
              :disabled="isLoading"
            />
          </UiFormControl>
        <UiFormMessage />
      </UiFormItem>
    </UiFormField>
  </form>
</template>
```

```vue
<template>
    <div class="grid gap-2">
      <UiButton :disabled="isLoading">
        <Loader2 v-if="isLoading" class="mr-2 h-4 w-4 animate-spin" />
        {{ $route.path === LOGIN_ROUTE ? 'Sign In with Email' : 'Sign Up with Email' }}
      </UiButton>
      <p class="text-sm text-[#72717a] dark:text-zinc-300">
        {{ $route.path === LOGIN_ROUTE ? `Don't have an account?` : 'Have an account?' }}
        <span
          @click="
            $route.path === LOGIN_ROUTE
              ? $router.push(REGISTRATION_ROUTE)
              : $router.push(LOGIN_ROUTE)
          "
          class="cursor-pointer underline underline-offset-4 hover:text-zinc-900 dark:hover:text-zinc-300/80"
        >
          {{ $route.path === LOGIN_ROUTE ? `Sign Up Now` : 'Sign In Now' }}
        </span>
      </p>
    </div>
</template>
```
````

</v-clicks>
