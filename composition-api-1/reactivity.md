# Reactivity





#### Reactive state

* declare reactive state with `ref`
* we can declare with initial value
* `ref` is an object with value property
* for template - directly use ref itself, for script use it's value property

```html
<script setup>
 import { ref } from 'vue'
 const count = ref(0); 
</script>

<template>
 <button @click="count++">{{ count }}</button>
</template>
```





