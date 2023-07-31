# List rendering





#### v-for

* used to render items in a list
* use unique value as index to be able to differentiate items in the list
* we can also use `of`

```html
<li v-for="(item, index) in items">
  {{ parentMessage }} - {{ index }} - {{ item.message }}
</li>
```



iterating Object properties

* will be the result of calling `Object.keys()`
* we can get value and key

```html
<li v-for="(value, key) in myObject">
  {{ key }}: {{ value }}
</li>
```





Range

* v-for can also take integer

```html
<span v-for="n in 10">{{ n }}</span>
```





With template

* v-for can be used with `<template>` just like `v-if`

```html
<ul>
  <template v-for="item in items">
    <li>{{ item.msg }}</li>
    <li class="divider" role="presentation"></li>
  </template>
</ul>
```



v-for and v-if

* to apply conditional rendering on individual elements of rendered list wrap `v-if` element with `v-for`

```html
<template v-for="todo in todos">
  <li v-if="!todo.isComplete">
    {{ todo.name }}
  </li>
</template>
```























