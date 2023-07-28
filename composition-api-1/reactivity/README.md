# Reactivity



{% hint style="info" %}

{% endhint %}



<img src="../../.gitbook/assets/file.excalidraw.svg" alt="" class="gitbook-drawing">





#### Reactive state

* declare reactive state with `ref`
* we can declare with initial value
* `ref` is an object with value property
* for template - directly use ref itself, for script use it's value property
* Vue uses dependency tracking alongside with refs to update template
* `ref` like `get` and `set` intercepts the write and read operations and updates template

```html
<script setup>
 import { ref } from 'vue'
 const count = ref(0); 
</script>

<template>
 <button @click="count++">{{ count }}</button>
</template>
```



Deep Reactivity

* `ref` enables reactivity for nested and complex objects&#x20;
* any updated value is detected





| Feature         | Ref                               | Reactive                       |
| --------------- | --------------------------------- | ------------------------------ |
| Stores          | Primitives and objects            | Objects only                   |
| Returns         | A reactive and mutable ref object | A reactive proxy of the object |
| Mutable         | Yes                               | No                             |
| Reactive        | Yes                               | Yes                            |
| Deep conversion | Yes                               | Yes                            |



reactive has limitations

* only works with object types
* can't replace the entire object
* when passing object's property to local variables or function reactivity connection will be lost





#### Ref Unwrapping

* works with nested inside a deep reactive object
* doesn't apply when it is accessed as a property of a shallow nested object

```javascript
const count = ref(0)
const state = reactive({
  count
})

console.log(state.count) // 0

state.count = 1
console.log(count.value) // 1
```



Ref inside Arrays and Collections

* no wrapping when the ref is an element of a reactive array

```javascript
const books = reactive([ref('Vue 3 Guide')])
// need .value here
console.log(books[0].value)

const map = reactive(new Map([['count', ref(0)]]))
// need .value here
console.log(map.get('count').value)
```



Unwrapping Templates

* unwrapped only if it is the final evaluated value

```html
<!-- Unwrapped -->
<div> {{ object.Id }} </div>

<!-- Can't be unwrapped -->
<div {{ object.Id + 1 }} </div>

```









