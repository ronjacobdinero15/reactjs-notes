# reactjs-notes

#$ npm installations

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
  content: ["./src/**/*.{html,js}"],
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

### supabase
```bash
npm i --save @supabase/supabase-js
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



