# Main configuracion Vue-Typescript
Main configuracion for a Vue js project with Typescript


## Run Locally

Install dependencies

```bash
 npm i @types/node
```

In the ``tsconfig.json`` add in the compilerOptions options : 

```bash
    "baseUrl": ".",
    "paths": {
        "@/*": ["./src/*"]
    }
```

Then, the ``vite.config.ts`` should look like this

```javascript
import { defineConfig } from 'vite';
import { resolve } from 'node:path';

import vue from '@vitejs/plugin-vue';

// https://vitejs.dev/config/
export default defineConfig({
	plugins: [vue()],
	resolve: {
		alias: [{ find: '@', replacement: resolve(__dirname, './src') }],
	},
});

```

Now run `npm run dev` and happy code.
## Badges

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)

