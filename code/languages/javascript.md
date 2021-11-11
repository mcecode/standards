# JavaScript

## Browser

### Globals

- Do not use the `window.` qualifier.

## Node.js

### Globals

- Do not `import` or `require` [Node.js globals](https://nodejs.org/api/globals.html).

### Modules

- Use the [`node:` URL scheme](https://nodejs.org/api/esm.html#esm_node_imports) to load Node.js core modules.
- Group `import`s and `require`s in the following order:
  - Node.js core modules
  - Modules from external packages
  - Project-specific modules
- Prefer to not destructure modules from external packages.
- Do not destructure Node.js core modules.
