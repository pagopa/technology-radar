---
title: "ECMAScript Modules"
ring: adopt
quadrant: "languages-and-frameworks"
tags: [javascript, nodejs, typescript]
---

[ECMAScript Modules (ESM)](https://nodejs.org/api/esm.html) is the official standard format to package JavaScript code for reuse. It was standardized in 2015 as part of ECMAScript 2015 (ES6) and provides a robust, unified way to write modular JavaScript code that works both in browsers and Node.js.

## Key Features

1. **Static Module Structure**: ESM's static `import` and `export` statements enable better static analysis, allowing tools to:
   - Perform tree-shaking (dead code elimination)
   - Optimize module loading
   - Create more efficient bundles

2. **Native Support**: Modern browsers and Node.js support ESM natively, eliminating the need for transpilation in many cases.

3. **Asynchronous by Design**: ESM supports both synchronous and asynchronous module loading, making it more flexible than CommonJS.

## Use Cases

- New JavaScript/TypeScript projects where module organization is important
- Projects that need to work in both browser and Node.js environments
- Libraries that need to be tree-shakeable
- Applications where bundle size optimization is critical

## Best Practices

1. Use the `.mjs` extension for pure ESM files or set `"type": "module"` in your `package.json`
2. Prefer named exports over default exports for better tooling support
3. Keep modules focused and single-responsibility
4. Use path aliases and module resolution to maintain clean import paths

Example of ESM syntax:
```javascript
// Importing
import { function1, function2 } from './module';
import * as module from './module';

// Exporting
export const myFunction = () => {};
export class MyClass {}
```

## Reference of usage in our organization

ESM is used in our modern TypeScript/JavaScript projects as the default module system. Examples include:

- Frontend applications built with Next.js
- React Native applications
- Node.js backend services
- Shared utility libraries

See also: [CommonJS](commonjs.md) (hold) for information about the legacy module system.
