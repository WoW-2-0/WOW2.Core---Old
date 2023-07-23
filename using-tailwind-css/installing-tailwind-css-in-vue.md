# Installing Tailwind CSS in Vue





* Install Tailwind CSS

```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

* Configure template paths

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

* Add the tailwind directives

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```
