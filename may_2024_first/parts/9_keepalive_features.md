# KeepAlive

<v-clicks>

#### Базовое использование: 

```vue
<KeepAlive>
  <component :is="activeComponent" />
</KeepAlive>
```
<div class="pt-16">

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