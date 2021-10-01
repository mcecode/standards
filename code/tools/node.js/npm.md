# npm

[npm](https://docs.npmjs.com) version when this document was last updated: 7.24.1

**Note:** This guide is for publishing npm packages, not for creating apps.

## Configuration files

### `package.json`

- Universal fields for all projects to include:
  - [`name`](https://docs.npmjs.com/cli/v7/configuring-npm/package-json#name)
  - [`version`](https://docs.npmjs.com/cli/v7/configuring-npm/package-json#version)
  - [`type`](https://nodejs.org/api/packages.html#packages_package_json_and_file_extensions)
  - [`license`](https://docs.npmjs.com/cli/v7/configuring-npm/package-json#license)
  - [`author`](https://docs.npmjs.com/cli/v7/configuring-npm/package-json#people-fields-author-contributors)
  - [`description`](https://docs.npmjs.com/cli/v7/configuring-npm/package-json#description-1)
  - [`keywords`](https://docs.npmjs.com/cli/v7/configuring-npm/package-json#keywords)
  - [`homepage`](https://docs.npmjs.com/cli/v7/configuring-npm/package-json#homepage)
  - [`bugs`](https://docs.npmjs.com/cli/v7/configuring-npm/package-json#bugs)
  - [`repository`](https://docs.npmjs.com/cli/v7/configuring-npm/package-json#repository)

### `.npmignore`

- For most use cases, it is better to use the [`files`](https://docs.npmjs.com/cli/v7/configuring-npm/package-json#files) field in `package.json` than a `.npmignore`.
- Uses the same syntax as a [`.gitignore`](../git.md#gitignore).
- More information about this file can be found [here](https://docs.npmjs.com/cli/v7/using-npm/developers#keeping-files-out-of-your-package).

### `.npmrc`

```ini
package-lock = false
```

**Note:** The rationale for including this setting can be found [here](https://github.com/eslint/eslint#why-doesnt-eslint-lock-dependency-versions) and [here](https://www.twilio.com/blog/lockfiles-nodejs).

## Standard file names

When applicable to the project, use the following file names:

- `./index.js`, as the main entry point
- `./cli.js`, as the main CLI executable

## Node.js support

- Prefer supporting only ECMAScript modules over CommonJS modules or both.
- Prefer following the [Node.js release cycle](https://nodejs.org/en/about/releases) and supporting only supported Node.js versions (i.e. Current, Active LTS, and Maintenance LTS releases).

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
