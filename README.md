![@bokub/prettier-config](https://user-images.githubusercontent.com/17952318/155517136-be39b194-d0ef-4fd6-8c47-dfef2de50a3e.png)

<h2>
<p align="center">
  My personal <a href="https://prettier.io">Prettier</a> config & workflow
</p>
  <p align="center">
  <a href="https://github.com/prettier/prettier"><img src="https://flat.badgen.net/badge/code%20style/prettier/ff69b4" alt="Code style"></a>
  <a href="https://www.npmjs.com/package/@bokub/prettier-config"><img src="https://flat.badgen.net/npm/dt/@bokub/prettier-config" alt="Downloads"></a>
  <a href="https://www.npmjs.com/package/@bokub/prettier-config"><img src="https://runkit.io/bokub/npm-version/branches/master/@bokub/prettier-config?style=flat" alt="Version"></a>
  </p>
</h2>

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
npx mrm@2 lint-staged
npx husky set .husky/pre-commit "npx lint-staged --concurrent false"
```

Then, in `package.json`, replace the `lint-staged` config with:

```json
"lint-staged": {
  "*": "prettier --write --ignore-unknown"
}
```

#### _Optional:_ Run prettier on existing code

```bash
npx prettier --write .
```

#### _Optional:_ Setup with ESLint

```bash
# With npm
npm i -D eslint-config-prettier eslint-plugin-prettier eslint

# With yarn
yarn add -D eslint-config-prettier eslint-plugin-prettier eslint
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

Then, in `package.json`, replace the `lint-staged` config (if it exists) with:

```json
  "lint-staged": {
    "*": "prettier --write --ignore-unknown",
    "*.{js,ts,vue}": "eslint --fix"
  }
```
