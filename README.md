# reactjs-notes

## On every React project (to make intellisense work on js files)
![autocomplete_intellisense_fixed](https://github.com/user-attachments/assets/422b71b3-b7c7-410e-a816-f5887f2f2d90)

Create a file in the root directory called:
```
jsconfig.json
```
Inside this file, copy and paste this:
```
{
  "compilerOptions": {
    "target": "ES6",
    "module": "commonjs",
    "jsx": "preserve",
    "allowSyntheticDefaultImports": true
  },
  "exclude": ["node_modules", "**/node_modules/*"],
  "include": ["src/**/*"]
}
```
Reference: 
[VSCode](https://code.visualstudio.com/docs/languages/jsconfig#_why-do-i-need-a-jsconfigjson-file)
[Udemy](https://www.udemy.com/course/the-ultimate-react-course/learn/lecture/38038174#questions/21582188)

## npm installations

### Vite
```bash
npm create vite@latest
```
```javascript
// .eslintrc.cjs

module.exports = {
  root: true,
  env: { browser: true, es2020: true },
  extends: [
    'eslint:recommended',
    'plugin:react/recommended',
    'plugin:react/jsx-runtime',
    'plugin:react-hooks/recommended',
  ],
  ignorePatterns: ['dist', '.eslintrc.cjs'],
  parserOptions: { ecmaVersion: 'latest', sourceType: 'module' },
  settings: { react: { version: '18.2' } },
  plugins: ['react-refresh'],
  rules: {
    'react-refresh/only-export-components': [
      'warn',
      { allowConstantExport: true },
    ],
    'no-unused-vars': 'warn',
    'react/prop-types': 'off',
  },
};
```

### Tailwind CSS with Vite
[Installation Documentation](https://tailwindcss.com/docs/guides/vite#react)

**OR**
```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

Copy and paste the content line
```javascript
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
Copy and paste this at the very top of **./src/index.css**
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Then (turn on/restart)
```bash
npm run dev
```

Then install this extension
```bash
Tailwind CSS IntelliSense
```

And install a special prettier extension (*this will automatically sort tailwind classes*)

[prettier-plugin-tailwindcss](https://github.com/tailwindlabs/prettier-plugin-tailwindcss)

**OR**
```bash
npm install -D prettier prettier-plugin-tailwindcss
```

Then create **.prettierrc** file then copy and paste this code in there:
```javascript
{
  "plugins": ["prettier-plugin-tailwindcss"]
}
```

### React Router
```bash
npm i react-router-dom
import { BrowserRouter as Router, Routes, Route } from 'react-router-dom'
```

### React Query
```bash
npm i @tanstack/react-query
```

### React Query DevTools
```bash
npm i @tanstack/react-query-devtools
```

### react icons
```bash
npm i react-icons
```

### react toast
```bash
npm i react-hot-toast
```

### react form
```bash
npm i react-hook-form
```

### Supabase
```bash
npm i --save @supabase/supabase-js
```

### styled-components
```bash
npm install styled-components
```

### Framer Motion
```bash
npm i framer-motion
```

### date-fns 
*(a very popular library for manipulating and for doing calculations with dates.)*
```bash
npm i date-fns
```

### Redux ToolKit
```bash
npm i @reduxjs/toolkit react-redux
```

### Redux DevTools
```bash
npm i @redux-devtools/extension
```

### JSON server (for fake api)
```bash
npm i json-server
```

### ESLint
```bash
npm i eslint vite-plugin-eslint eslint-config-react-app --save-dev
```

### lodash
```bash
npm i lodash
import _  from 'lodash'
```



