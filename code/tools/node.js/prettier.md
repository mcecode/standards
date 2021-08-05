# Prettier

[Prettier](https://prettier.io/docs/en/index.html) version when this document was last updated: 2.3.2

## Installation

```console
npm i -DE prettier
```

**Note:** The `-E` or `--save-exact` option is required because Prettier changes how it formats code with each release. As stated in the [Prettier documentation](https://prettier.io/docs/en/install.html),

> ... we change how code is formatted in each release! It’s important to have a locked down version of Prettier in your `package.json`.

## Configuration files

### `.prettierignore`

- Include project-specific directories and files that need to be ignored by Prettier.
- Uses the same syntax as a `.gitignore`.
- Prettier ignores the `node_modules` directory by default, so there is no need to add it here.

### `.prettierrc.json`

```json
{
  "trailingComma": "none"
}
```

## Running the CLI

### Using `npx`

Lint files:

```console
npx prettier . -c
```

Format files:

```console
npx prettier . -w
```

### Using `npm scripts`

In `package.json`:

```json
{
  "scripts": {
    "lint": "prettier . -c",
    "format": "prettier . -w"
  }
}
```

Lint files:

```console
npm run lint
```

Format files:

```console
npm run format
```
