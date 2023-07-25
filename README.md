# Creating an App



App start progress

* Creating an instance
* Adding components&#x20;
* Mounting&#x20;
*











* **Mounting** -
* process of injecting a Vue component into DOM
* app instance is mounted to the **Root** component
* Root component must have id of **app**

```html
<body>
    <!-- Root componen -->
    <div id="app"></div> 
</body>
```





* Vue application is started by creating a new application instance with `createApp`

```javascript
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{vue,js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```











Practice

#### -

