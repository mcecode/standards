# markdownlint

[markdownlint](https://github.com/DavidAnson/markdownlint) version when this document was last updated: 0.25.1 \
[markdownlint-cli2](https://github.com/DavidAnson/markdownlint-cli2) version when this document was last updated: 0.4.0

## Installation

```console
npm i -D markdownlint-cli2
```

**Note:** There is also a [markdownlint-cli](https://github.com/igorshubovych/markdownlint-cli). However, this document advocates the use of markdownlint using markdownlint-cli2, that is why that is the package to be installed.

## Rules

A complete list of markdownlint rules can be found [here](https://github.com/DavidAnson/markdownlint/blob/main/doc/Rules.md).

## Configuration files

**Note:** [markdownlint-cli2 does not support ignore files](https://github.com/DavidAnson/markdownlint-cli2#compatibility).

### `.markdownlint.jsonc`

````jsonc
{
  // MD003 - Heading style
  "MD003": {
    // Example:
    // # Heading
    "style": "atx"
  },

  // MD004 - Unordered list style
  "MD004": {
    // Example:
    // - Unordered list item
    "style": "dash"
  },

  // MD009 - Trailing spaces
  "MD009": {
    // Do not use trailing spaces to induce line breaks, use a backslash (\)
    // instead
    "br_spaces": 0
  },

  // MD013 - Line length
  // Do not restrict line length
  "MD013": false,

  // MD024 - Multiple headings with the same content
  "MD024": {
    // Allow headings with the same content if they are not within the same
    // nesting
    "siblings_only": true
  },

  // MD029 - Ordered list item prefix
  "MD029": {
    // Example:
    // 1. Number one
    // 2. Number two
    // 3. Number three
    "style": "ordered"
  },

  // MD033 - Inline HTML
  // Allow inline HTML
  "MD033": false,

  // MD035 - Horizontal rule style
  "MD035": {
    // Example:
    // ...content
    // ---
    // ...content
    "style": "---"
  },

  // MD048 - Code fence style
  "MD048": {
    // Example:
    // ```js
    // console.log("Hello world!");
    // ```
    "style": "backtick"
  },

  // MD049 - Emphasis style should be consistent
  "MD049": {
    // Example:
    // _Emphasis_
    "style": "underscore"
  },

  // MD050 - Strong style should be consistent
  "MD050": {
    // Example:
    // **Strong**
    "style": "asterisk"
  }
}
````

## Run

### Using npx

Lint and fix files ending in `.md` while ignoring the `node_modules` directory:

```console
npx markdownlint-cli2-fix "**/*.md" "#node_modules"
```

### Using npm scripts

In `package.json`:

```json
{
  "scripts": {
    "lint": "markdownlint-cli2-fix \"**/*.md\" \"#node_modules\""
  }
}
```

Lint and fix files ending in `.md` while ignoring the `node_modules` directory:

```console
npm run lint
```
