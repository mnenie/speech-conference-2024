# KeepAlive

<v-clicks>

#### Базовое использование: 

```vue
<KeepAlive>
  <component :is="activeComponent" />
</KeepAlive>
```
<v-clicks>

<h4 class="pt-16"> Props</h4>

```ts{*|3|4|5}
type MatchPattern = string | RegExp | (string | RegExp)[];
export interface KeepAliveProps {
    include?: MatchPattern;
    exclude?: MatchPattern;
    max?: number | string;
}
```

</v-clicks>

</v-clicks>