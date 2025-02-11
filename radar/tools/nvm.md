---
title: "nvm"
ring: hold
quadrant: "tools"
tags: [typescript, nodejs]
---

[nvm](https://github.com/nvm-sh/nvm) is a version manager for node.js, designed
to be installed per-user, and invoked per-shell. It is a common tool for
managing multiple versions of Node.js and is used by many developers.

Despite we've used it in the past, we are not using it anymore since we've
replaced it with [nodenv](https://github.com/nodenv/nodenv) which offers a
similar functionality but it's more flexible and maintained.

We observed that nodenv has a minimal impact on system performance (i.e. doesn't
freeze zsh shell when switching between directories) and offers
[greater flexibility](https://github.com/nodenv/nodenv/wiki/Why-nodenv%3F) in
configuring development environments.
