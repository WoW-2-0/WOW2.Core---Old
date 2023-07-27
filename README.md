# Options API









Options API





When

* creating low complexity components
* progressive enhancement



* centered around the concept of "component instance"
* easy for developers with OOP language backgrounds









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





#### Options API[​](https://vuejs.org/guide/introduction.html#options-api) <a href="#options-api" id="options-api"></a>

With Options API, we define a component's logic using an object of options such as `data`, `methods`, and `mounted`. Properties defined by options are exposed on `this` inside functions, which points to the component instance:



