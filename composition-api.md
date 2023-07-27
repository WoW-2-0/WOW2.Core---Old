# Composition API





When

* full application with Vue



* centered around reactive state variables directly in a function scope
* composes state from multiple functions together to handle complexity



```html
<script>

import { ref } from 'vue'

export default {
    setup() {
        const count = ref(0);
        
        function increment() {
            count.increment++;
}
        return {
            count, 
            increment
        }
    }
}    

</script>
```









Short version



```html
<script setup>

import { ref } from 'vue'

const count = ref(0);

function increment() {
   count.increment++;
   
</script>
```

