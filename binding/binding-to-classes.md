# Binding to Classes







* bind to objects



```html
<template>
    <div :class="style"></div> 
</template>

<script setup>
    const status = ref(false);
    const style = computed(() => {
        return {
            'active': status
        }
    });

</setup>
```





* binding inline

```html
<template>
    <div :class="[status ? active : '']"></div> 
</template>

<script setup>
    const status = ref(false);
</setup>
```



* binding as array

```html
<template>
    <div :class="[activeClass, errorClass]"></div>
    <div :class="[{active : isActive}, errorClass]"></div>
</template>

<script setup>
    const isActive = ref(false);
    const activeClass = ref('active');
    const errorClass = ref('text-danger');
</setup>
```





