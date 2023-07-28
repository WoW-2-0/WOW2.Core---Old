# Binding







#### Text Interpolation

* use curly braces syntax

```html
<span>Message: {{ msg }}</span>
```





**Attribute binding**

* use `v-bind` to bind to HTML attributes, use `:` for shorthand&#x20;
* this works for [boolean attributes](https://html.spec.whatwg.org/multipage/common-microsyntaxes.html#boolean-attributes) too
* for multiple attributes we can bind an object with `v-bind`

```html
<div v-bind:id="dynamicId"></div>

<!-- shorthand version -->
<div :id="dynamicId"></div>

<!-- boolean attribute -->
<div :disabled="isDisabled"></div>

<!-- binding multiple attributes -->
<div v-bind="objectOfAttrs"></div>

<!-- script -->
const objectOfAttrs = {
  id: 'container',
  class: 'wrapper'
}
```



#### Expressions

* Vue supports full `JS` expressions inside all data bindings
* each expression can only have one expression
* we can also call functions in expressions - they are called every time component updates

```html
<!-- text interpolation -->
<span>
    Message - {{ warning.Code + warning.Message }}
</span>

<!-- single expression -->
<span>
    Message - {{ isStatusOk() ? `YES` : `NO` }}    
</span>

<!-- attribute binding -->
<div :disabled="isDisabled(item)"></div>

```



