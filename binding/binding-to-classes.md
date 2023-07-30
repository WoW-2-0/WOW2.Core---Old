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



Binding with Components

* will be applied to root element and merge with any existing classes
* if root element is not a single element, need to specify which element must receive it

```html
<!-- single root element -->
<MyComponent :class="{ active: isActive }" />

<!-- render -->
<p class="foo bar active"></p>

<!-- multiple root element -->
<MyComponent class="baz" />

<!-- component -->
<p :class="$attrs.class">Hi!</p>
<span>This is a child component</span>

<!-- render -->
<p class="baz">Hi!</p>
<span>This is a child component</span>

```



#### Binding Inline Styles

* supports binding JS objects to style
* camelCase for CSS rules are recommended, kebab-case also supported
* can be bound to arrays - of multiple objects will be merged
* Vue auto adds vendor prefix
* multiple values can be applied and the one which is supported by browser will be used

```html
<!-- recommended -->
<div :style="{ color: activeColor, fontSize: fontSize + 'px' }"></div>

<!-- kebab csae -->
<div :style="{ 'font-size': fontSize + 'px' }"></div>

<!-- binding to an object -->
<div :style="styledObject"></div>

<!-- binding to an array -->
<div :style=[baseStyle, overridingStyle]"></div>

<!-- binding with multiple valeus -->
<div :style="{ display: ['-webkit-box', '-ms-flexbox', 'flex'] }></div>
```
