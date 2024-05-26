# Смотрим что в `script`

````md magic-move

```ts
const formSchema = toTypedSchema(
  z.object({
    email: z
      .string({ required_error: 'Email is a required field' })
      .nonempty('Email is a required field')
      .email('Email must be a valid'),
    password: z
      .string({ required_error: 'Password is a required field' })
      .nonempty('Password is a required field')
      .min(8, 'Password must be at least 8 characters')
  })
);

const { handleSubmit, isFieldDirty } = useForm({
  validationSchema: formSchema
});

const { value: email } = useField<string>('email');
const { value: password } = useField<string>('password');
```

```ts
const authStore = useAuthStore();
const { isLoading } = storeToRefs(authStore);

const route = useRoute();
const localPath = useLocalePath();

const onSubmit = handleSubmit(async (values) => {
  try {
   ... // все что относится к onSubmit
  } catch (err) {
    console.log(err);
  }
});
```

```ts
// хуки для кэшированного компонента
onActivated(() => {
  console.log('activated');
});

onDeactivated(() => {
  console.log('deactivated');
});

// посмотрим на хуки монтирования и размонтирования
onMounted(() => {
  console.log('mounted');
});

onUnmounted(() => {
  console.log('unmounted');
});

// mounted, activated, deactivated, mounted, activated, deactivated, activated, deactivated ...
```

````

