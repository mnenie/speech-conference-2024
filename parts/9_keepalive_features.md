# KeepAlive

<v-clicks>

#### Базовое использование: 

```vue
<KeepAlive>
  <component :is="activeComponent" />
</KeepAlive>
```

```vue
<KeepAlive>
  <comp-a v-if="a > 1"></comp-a>
  <comp-b v-else></comp-b>
</KeepAlive>
```
<div class="pt-4">

#### Props

```ts
type MatchPattern = string | RegExp | (string | RegExp)[];
export interface KeepAliveProps {
    include?: MatchPattern;
    exclude?: MatchPattern;
    max?: number | string;
}
```

</div>

</v-clicks>