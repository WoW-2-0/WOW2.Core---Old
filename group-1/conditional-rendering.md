# Conditional Rendering

#### v-if

* conditionally renders a block

```html
<h1 v-if="awesome">Vue is awesome!</h1>
```

#### v-else

* used for else block of if
* `v-else` must follow `v-if` or `v-else-if` blocks&#x20;

```html
<h1 v-if="awesome">Vue is awesome!</h1>
<h1 v-else>Oh no 😢</h1>
```

#### v-else-if

* serves as `else if` block
* `v-else-if` must follow `v-if` or `v-else-if` blocks

```html
<div v-if="type === 'A'"> A </div>
<div v-else-if="type === 'B'"> B </div>
<div v-else-if="type === 'C'"> C</div>
<div v-else> Not A/B/C </div>
```

#### v-show

*



#### Best Practices



#### v-if on \<template>

* v-if is a directive, so it must be attached to a single element
* if we want to toggle multiple elements, we must use `v-if` on `template` block

```html
<template v-if="ok">
  <h1>Title</h1>
  <p>Paragraph 1</p>
  <p>Paragraph 2</p>
</template>
```

#### v-if

#### v-if

