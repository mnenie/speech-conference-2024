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

<!-- пропсы: 
include - включает компоненты в кэширование

exclude - исключает

max - Мы можем ограничить максимальное количество экземпляров компонентов, которые можно кэшировать с помощью опции max. Когда max задан, <KeepAlive> ведет себя как LRU cache: если количество закэшированных экземпляров вот-вот превысит указанное максимальное количество, то наименее недавно использованный закэшированный экземпляр будет уничтожен, чтобы освободить место для нового. -->