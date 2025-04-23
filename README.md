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

Inside **next.config.ts**:
```bash
import type { NextConfig } from "next"
import type { RuleSetRule } from "webpack"

const nextConfig: NextConfig = {
  webpack(config) {
    const fileLoaderRule = config.module.rules.find(
      (rule: RuleSetRule) =>
        rule.test instanceof RegExp && rule.test.test(".svg"),
    )

    config.module.rules.push(
      {
        ...fileLoaderRule,
        test: /\.svg$/i,
        resourceQuery: /url/, // *.svg?url
      },
      {
        test: /\.svg$/i,
        issuer: fileLoaderRule.issuer,
        resourceQuery: { not: [...fileLoaderRule.resourceQuery.not, /url/] }, // exclude if *.svg?url
        use: ["@svgr/webpack"],
      },
    )

    fileLoaderRule.exclude = /\.svg$/i

    return config
  },
}

export default nextConfig
```

Install
```bash
npm install --save-dev @types/webpack
```

Inside **tsconfig.json**, add **"./*"** to the paths array:
```bash
"paths": {
  "@/*": ["./src/*", "./*"]
}
```

Create **svgr.d.ts** at the root of your repo and paste:
```bash
declare module "*.svg" {
  import { FC, SVGProps } from "react"
  const content: FC<SVGProps<SVGElement>>
  export default content
}

declare module "*.svg?url" {
  import { StaticImageData } from "next/image"

  const content: StaticImageData
  export default content
}
```

Add the type declaration file to your **tsconfig.json**'s include array. Ensure it's the first item:
```bash
{
  "include": [
    "svgr.d.ts",
    "next-env.d.ts",
    "**/*.ts",
    "**/*.tsx",
    ".next/types/**/*.ts"
  ]
  // ...other config
}
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
