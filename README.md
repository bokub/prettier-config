# @bokub / prettier-config

[![Code style][style-src]][style-href]
[![Downloads][downloads-src]][downloads-href]
[![Version][version-src]][version-href]

> My personal [Prettier](https://prettier.io) config / workflow

#### Install

```bash
# With npm
npm i -D prettier @bokub/prettier-config

# With yarn
yarn add -D prettier @bokub/prettier-config
```

#### Add the following to your `package.json`:

```json
{
  "prettier": "@bokub/prettier-config"
}
```

#### _Optional:_ Setup pre-commit hook with husky

```bash
# With npm
npx husky-init
npm i -D pretty-quick
npx husky set .husky/pre-commit "npx pretty-quick --staged"

# With yarn
npx husky-init # add --yarn2 for Yarn 2
yarn add -D pretty-quick
yarn husky set .husky/pre-commit "npx pretty-quick --staged"
```

#### _Optional:_ Run prettier on existing code

```bash
npx prettier --write .
```

#### _Optional:_ Setup with ESLint

```bash
# With npm
npm i -D eslint-config-prettier eslint-plugin-prettier eslint@latest

# With yarn
yarn add -D eslint-config-prettier eslint-plugin-prettier eslint@latest
```

Then, edit your ESLint configuration file:

```jsonc
{
  "plugins": ["prettier"],
  "extends": ["<some-config>", "plugin:prettier/recommended"], // Add to the end of the array
  "rules": {
    "prettier/prettier": "warn" // Optionally, you can set the error level to warn
  }
}
```

[style-src]: https://flat.badgen.net/badge/code%20style/prettier/ff69b4
[style-href]: https://github.com/prettier/prettier
[downloads-src]: https://flat.badgen.net/npm/dt/@bokub/prettier-config
[downloads-href]: https://www.npmjs.com/package/@bokub/prettier-config
[version-src]: https://runkit.io/bokub/npm-version/branches/master/@bokub/prettier-config?style=flat
[version-href]: https://www.npmjs.com/package/@bokub/prettier-config
