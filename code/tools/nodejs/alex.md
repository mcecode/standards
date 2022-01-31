# alex

[alex](https://github.com/get-alex/alex) version when this document was last updated: 9.1.0

## Installation

```console
npm i -D alex
```

## Rules

alex uses [retext-equality](https://github.com/retextjs/retext-equality) and [retext-profanities](https://github.com/retextjs/retext-profanities) rules, a full list of which can be found [here](https://github.com/retextjs/retext-equality/blob/main/rules.md) and [here](https://github.com/retextjs/retext-profanities/blob/main/rules.md), respectively.

## Configuration files

### `.alexignore`

- Include project-specific directories and files that need to be ignored by alex.
- Uses the same syntax as a [`.gitignore`](../git.md#gitignore).
- alex ignores the `node_modules` directory by default, so there is no need to add it here.

### `.alexrc.js`

```js
exports.noBinary = true;
exports.profanitySureness = 1;
```

## Running the CLI

### Using npx

Lint files:

```console
npx alex .
```

### Using npm scripts

In `package.json`:

```json
{
  "scripts": {
    "lint": "alex ."
  }
}
```

Lint files:

```console
npm run lint
```
