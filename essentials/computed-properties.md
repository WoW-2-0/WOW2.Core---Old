# Computed Properties



#### When

* expression in template is complex
* expression must be reusable
* works by caching the value
* not evaluated until any of dependencies is updated
* more efficient than a function



```javascript
const message = computed(() => status ? "Success" : "Failed");
```

