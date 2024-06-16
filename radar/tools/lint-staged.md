---
title: "lint-staged"
ring: adopt
quadrant: "tools"
tags: [git]
---

[lint-staged](https://github.com/lint-staged/lint-staged#readme) is a tool that
allows to easily run linters against staged git files. We use it in our
pre-commit hook usually in combination with Husky.

## Use cases

For example to run the linter and the prettier on all staged typescript or
javascript files and prettier on all json or md files, before committing, a
configuration like the following can be used:

- in `.husky/pre-commit`:

```bash
#!/usr/bin/env sh
. "$(dirname -- "$0")/_/husky.sh"

npx lint-staged --allow-empty
```

- and in `package.json`:

```json
{
  "lint-staged": {
    "*.{js,jsx,ts,tsx}": ["eslint -c .eslintrc.js --fix", "prettier --write"],
    "*.{json,md}": ["prettier --write"]
  }
}
```

## Reference of usage in our organization

A non exhaustive list of our projects that use Husky:

- [io-app](https://github.com/pagopa/io-app)
- [io-web-profile](https://github.com/pagopa/io-web-profile)
- [pagopa-editorial-components](https://github.com/pagopa/pagopa-editorial-components)
- [developer-portal](https://github.com/pagopa/developer-portal)
