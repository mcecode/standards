# npm

[npm](https://docs.npmjs.com/) version when this document was last updated: 7.20.3

**Note:** This guide is for publishing npm packages, not for creating apps.

## Configuration files

### `package.json`

- Universal fields for all projects to include:
  - `name`
  - `version`
  - `license`
  - `author`
  - `description`
  - `keywords`
  - `homepage`
  - `bugs`
  - `repository`
- Other fields that a project may need can be found in the [`package.json` documentation](https://docs.npmjs.com/cli/v7/configuring-npm/package-json).

### `.npmignore`

- For most use cases, it is better to use the [`files`](https://docs.npmjs.com/cli/v7/configuring-npm/package-json#files) field in `package.json` than a `.npmignore`.
- More information about this file can be found [here](https://docs.npmjs.com/cli/v7/using-npm/developers#keeping-files-out-of-your-package).

### `.npmrc`

```ini
package-lock = false
```

**Note:** The rationale for including this setting can be found [here](https://github.com/eslint/eslint#why-doesnt-eslint-lock-dependency-versions) and [here](https://www.twilio.com/blog/lockfiles-nodejs).

## Steps to publish a package

1. Run tests and linters.
2. Update version in `package.json`.
3. Update `CHANGELOG.md`.
4. If necessary, run a build command.
5. If necessary, test with [`npm link`](https://docs.npmjs.com/cli/v7/commands/npm-link).
6. Run [`npm puslish`](https://docs.npmjs.com/cli/v7/commands/npm-publish).
7. Commit release to Git.
8. Add a release Git tag.
9. Push release commit and tag to GitHub.
10. Create a GitHub release based on `CHANGELOG.md` using the release tag.
