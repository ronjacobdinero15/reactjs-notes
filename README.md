# reactjs-notes

## npm installations

install a special prettier extension (*this will automatically sort tailwind classes*)

[prettier-plugin-tailwindcss](https://github.com/tailwindlabs/prettier-plugin-tailwindcss)

**OR**
```bash
npm install -D prettier prettier-plugin-tailwindcss
```

Then create **.prettierrc** file then copy and paste this code in there:
```javascript
{
  "plugins": ["prettier-plugin-tailwindcss"],
  "semi": false
}
```

### SVGR
```bash
npm install --save-dev @svgr/webpack
```

### react-error-boundary
```bash
npm i react-error-boundary
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
```
<Toaster
  position="top-center"
  gutter={12}
  containerStyle={{ margin: '8px' }}
  toastOptions={{
    success: {
      duration: 3000,
    },
    error: {
      duration: 5000,
    },
    style: {
      fontSize: '16px',
      maxWidth: '800px',
      padding: '16px 24px',
    },
  }}
/>
```

### react form
```bash
npm i react-hook-form
```

### Supabase
```bash
npm i @supabase/supabase-js
```

### styled-components
```bash
npm install styled-components
```

### Framer Motion
```bash
npm i framer-motion
```

### Recharts
```bash
npm i
```bash
npm install recharts
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

### lodash
```bash
npm i lodash
import _  from 'lodash'
```
