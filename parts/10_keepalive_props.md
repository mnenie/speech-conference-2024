# Применение KeepAlive Props

<v-clicks>

````md magic-move
```vue
//include

<KeepAlive :include="['a', 'b']">
  <component :is="activeComponent" />
</KeepAlive>
```

```vue
//include

<KeepAlive :include="/a|b/">
  <component :is="activeComponent" />
</KeepAlive>
```

```vue
//include

<KeepAlive include="a,b">
  <component :is="activeComponent" />
</KeepAlive>
```
````

````md magic-move
```vue
//exclude

<KeepAlive :exclude="['a', 'b']">
  <component :is="activeComponent" />
</KeepAlive>
```

```vue
//exclude

<KeepAlive :exclude="/a|b/">
  <component :is="activeComponent" />
</KeepAlive>
```

```vue
//exclude

<KeepAlive exclude="a,b">
  <component :is="activeComponent" />
</KeepAlive>
```
````

```vue
//max

<KeepAlive :max="10">
  <component :is="activeComponent" />
</KeepAlive>
```

</v-clicks>