# ESLint

[ESLint](https://eslint.org) version when this document was last updated: 7.32.0 \
[eslint-config-mcecode](https://github.com/mcecode/eslint-config-mcecode) version when this document was last updated: 1.0.0

## Installation

```console
npm i -D eslint-config-mcecode
```

**Note:** eslint-config-mcecode is installed instead of ESLint because it is the default configuration that will be used, and it states ESLint as a peer dependency which npm version 7 will install with it.

## Rules

A complete list of ESLint rules can be found [here](https://eslint.org/docs/rules).

## Configuration files

### `.eslintignore`

- Include project-specific directories and files that need to be ignored by ESLint.
- Uses the same syntax as a [`.gitignore`](../git.md#`.gitignore`).
- ESLint ignores the `node_modules` directory by default, so there is no need to add it here.

### `.eslintrc.json`

```jsonc
{
  "env": {
    "es2021": true

    // ... other global environments, see:
    // https://eslint.org/docs/user-guide/configuring/language-options#specifying-environments
  },
  "parserOptions": {
    "ecmaVersion": "latest",

    // If using ESModules, add:
    "sourceType": "module"
  },
  "extends": "mcecode",
  "reportUnusedDisableDirectives": true
}
```

## Running the CLI

### Using npx

Lint files:

```console
npx eslint . --cache --cache-location node_modules -f codeframe
```

### Using npm scripts

In `package.json`:

```json
{
  "scripts": {
    "lint": "eslint . --cache --cache-location node_modules -f codeframe"
  }
}
```

Lint files:

```console
npm run lint
```
