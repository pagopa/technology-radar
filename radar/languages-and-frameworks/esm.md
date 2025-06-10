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

## Best Practices

1. Set `"type": "module"` in your `package.json` or use the `.mjs` extension (`.mts` on TypeScript) for pure ESM files
2. Prefer named exports over default exports for better tooling support

Example of ESM syntax:

```javascript
// Importing
import { function1, function2 } from './module.js';
import * as module from './module.js';

// Exporting
export const myFunction = () => {};
export class MyClass {}
```

### Why are extension mandatory?

ESM requires explicit file extensions in import statements to ensure clarity and avoid ambiguity. This is a design choice that helps the JavaScript engine resolve modules correctly, especially in environments where both ESM and CommonJS coexist.

When working with TypeScript, you still need to specify the `.js` file extension in your import statements, even if the original file is a TypeScript file.
 
## Typescript Support

To use ESM in TypeScript, you need to configure your `tsconfig.json` file appropriately. Here’s an example configuration:

```json
{
  "compilerOptions": {
    "module": "NodeNext", // Output ESM format
    "moduleResolution": "NodeNext", // Use Node's module resolution algorithm
  }
}
```
