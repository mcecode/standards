# ESLint

[ESLint](https://eslint.org) version when this document was last updated: 8.8.0 \
[eslint-config-mcecode](https://github.com/mcecode/eslint-config-mcecode) version when this document was last updated: 2.0.0

## Installation

```console
npm i -D eslint-config-mcecode
```

**Note:** eslint-config-mcecode is installed instead of ESLint because it is the default configuration that will be used, and it states ESLint as a peer dependency which npm version 7 or later will install with it.

## Rules

A complete list of ESLint rules can be found [here](https://eslint.org/docs/rules).

## Configuration files

### `.eslintignore`

- Include project-specific directories and files that need to be ignored by ESLint.
- Uses the same syntax as a [`.gitignore`](../git.md#gitignore).
- ESLint ignores the `node_modules` directory by default, so there is no need to add it here.

### `.eslintrc.json`

```jsonc
{
  "env": {
    // For a list of global environments, see:
    // https://eslint.org/docs/user-guide/configuring/language-options#specifying-environments
  },
  "parserOptions": {
    // If using a transpiler, add:
    "ecmaVersion": "latest",
    // Else, set 'ecmaVersion' based on target environments' supported
    // ECMAScript version. See:
    // https://kangax.github.io/compat-table/es6
    // https://node.green

    // If using ECMAScript modules, add:
    "sourceType": "module"
  },
  "extends": "mcecode",
  "reportUnusedDisableDirectives": true

  // If specific files need different settings, see:
  // https://eslint.org/docs/user-guide/configuring/configuration-files#how-do-overrides-work
}
```

## Running the CLI

### Using npx

Lint files:

```console
npx eslint . --cache --cache-location node_modules
```

### Using npm scripts

In `package.json`:

```json
{
  "scripts": {
    "lint": "eslint . --cache --cache-location node_modules"
  }
}
```

Lint files:

```console
npm run lint
```
