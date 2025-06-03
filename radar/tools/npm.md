---
title: "NPM"
ring: hold
quadrant: "tools"
tags: [nodejs]
---

npm is the default package manager for Node.js and the largest ecosystem of open source libraries in the JavaScript world. It provides a straightforward way to manage project dependencies, publish packages, and handle scripts for development workflows.

However, npm's traditional approach to dependency resolution via the `node_modules` directory can lead to "ghost dependencies"—cases where a package can access dependencies it does not explicitly declare, simply because they are present somewhere in the dependency tree. This can cause hidden bugs, unpredictable builds, and makes it harder to reason about project dependencies.

**Why on hold:**

To avoid ghost dependencies and improve reliability, we recommend using [pnpm](https://pnpm.io/) or other modern alternatives that enforce strict dependency boundaries and offer better performance and disk efficiency.