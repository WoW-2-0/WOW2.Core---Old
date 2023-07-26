# API Styles















* Both fully capable of covering common use cases
* `Options API` is implemented on top of `Composition API`

















Example

* Options API

```javascript
<template>
  <button class="p-4 py-2 bg-white bg-opacity-10 border border-1
         border-slate-300 rounded-lg font-bold text-slate-300"
         @click="increment">
    Count is {{ count }}
  </button>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  // reactive state
  data() {
    return {
      count: 0
    };
  },

  // functions
  methods: {
    increment() {
      this.count++;
    },
  },

  // hooks
  mounted() {
    console.log(`The initial count in options API is ${this.count}.`);
  }
});

</script>
```



* Composition API

```javascript
<template>
  <button class="p-4 py-2 bg-white bg-opacity-10 border border-1 
          border-slate-300 rounded-lg font-bold text-slate-300"
          @click="increment">
    Count is {{ count }}
  </button>
</template>


<script setup lang="ts">
import {onMounted, ref} from "vue";

// reactive state
const count = ref(0);

// functions
function increment() {
  count.value++;
}

// hooks
onMounted(() => {
  console.log(`The initial count is ${count.value}.`);
});
</script>vue
```





