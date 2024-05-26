# Как это работает?

<div class="flex items-start gap-8">

<img class="w-1/2" src="/form.png" />

<div class="flex flex-col gap-4">
<v-clicks>

```ts
onMounted(() => {
  route.path === REGISTRATION_ROUTE
    ? console.log('форма создалась в registration')
    : console.log('форма создалась в login');
});
```

<img class="w-96" src="/console.png" />
</v-clicks>
</div>
</div>
