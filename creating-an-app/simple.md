---
description: Creating simple Vue app with template and style
---

# Simple







Project files

*

#### Creating a Vue app with some style

Initialize project

* Create folder for the project
* Create template file - `index.html`
* Create script file - `app.js`
* Copy logo.png into project folder



Create script

* Create app instance
* Create hello component
* Register hello component
* Mount app to root element

```javascript
let app = Vue.createApp({
  data() {
    return {
      count: 0
    }
  }
});

app.component("hello", {
  template: `<h1 class="text-green-300 text-center text-3xl">{{ message }}</h1>`,
  data() {
    return {
      message: "Hello World!",
    };
  },
});

app.mount('#app');
```

Create template

* Create template base
* Add root element
* Add Vue and Tailwind script
* Add app.js script
* Create logo along with hello component int the center

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport"
        content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://unpkg.com/vue@next"></script>
</head>

<body class="bg-[#1a1a1a]">
  <div id="app">

    <div class="content h-screen w-full flex items-center justify-center">
      <div class="flex-column items-center justify-center space-y-10">
        <img src="./logo.png"
             alt="Vue logo"
             class="h-40 w-40">
        <hello></hello>
      </div>
    </div>

  </div>

  <script src="app.js"></script>
</body>

</html>
```



* Open with Live Server
