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



Writable

```javascript
const fullName = computed({
    // getter
    get() {
        return firstName.value + ' ' + lastName.value;
    },
    
    // setter
    set() {
        [firstName.value, lastName.value] = newValue.split()
    }    
});
```





#### How

* getter must be side effect free
* don't make async requests in getter
* don't mutate value returned by computed property - it's just a snapshot

