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

* element will be rendered and added to DOM, but will be toggled by `display` property
* doesn't support `template` element or `v-else` block

####

####

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

#### v-if vs v-show

* `v-if` is "real" conditional rendering, it ensures proper destruction of child components
* `v-if` is lazy, if condition is false in first render, conditional block won't be rendered
* `v-show` always renders the block, if condition is false, hides with display property
* `v-if` has higher toggle and `v-show` has initial render costs
* `v-if` is used if condition doesn't change at runtime and `v-show` used if toggle is very often&#x20;

#### v-if with v-for

* never use v-if with v-for
*

