# List rendering





#### v-for

* used to render items in a list
* use unique value as index to be able to differentiate items in the list
* we can also use `of`
* doesn't pass data to components when used directly with them, instead data is passed with props
* Vue detects mutation in source collection and updates DOM accordingly





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



Maintaining state with key

* use `key` attribute to let Vue keep track of elements in DOM and in array
* use primitive values for `key`

```html
<div v-for="item in items" :key="item.id">
  <!-- content -->
</div>
```





















