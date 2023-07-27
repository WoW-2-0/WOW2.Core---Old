# Reactivity



{% hint style="info" %}

{% endhint %}



<img src="../.gitbook/assets/file.excalidraw.svg" alt="" class="gitbook-drawing">





#### Reactive state

* declare reactive state with `ref`
* we can declare with initial value
* `ref` is an object with value property
* for template - directly use ref itself, for script use it's value property
* Vue uses dependency tracking alongside with refs to update template

```html
<script setup>
 import { ref } from 'vue'
 const count = ref(0); 
</script>

<template>
 <button @click="count++">{{ count }}</button>
</template>
```





