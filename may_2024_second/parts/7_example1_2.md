### Событие onInput
```ts
@input="(e: Event) => (msg = (e.target as HTMLInputElement).value)"
```
<v-clicks>

````md magic-move
```ts{1}
(e) //event
```
```ts{3}
(e) //event

e.target as HTMLInputElement
```
```ts{5}
(e) //event

e.target as HTMLInputElement

.value
```
````

<img src="/input.png" class="h-72" />

</v-clicks>