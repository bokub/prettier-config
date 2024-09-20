![@bokub/prettier-config](https://user-images.githubusercontent.com/17952318/155517136-be39b194-d0ef-4fd6-8c47-dfef2de50a3e.png)

<h2>
<p align="center">
  My personal <a href="https://prettier.io">Prettier</a> config & workflow
</p>
  <p align="center">
  <a href="https://github.com/prettier/prettier"><img src="https://flat.badgen.net/badge/code%20style/prettier/ff69b4" alt="Code style"></a>
  <a href="https://www.npmjs.com/package/@bokub/prettier-config"><img src="https://flat.badgen.net/npm/dt/@bokub/prettier-config" alt="Downloads"></a>
  <a href="https://www.npmjs.com/package/@bokub/prettier-config"><img src="https://gradgen.bokub.workers.dev/npm/v/@bokub/prettier-config?gradient=b65cff,11cbfa&style=flat&label=version" alt="Version"></a>
  </p>
</h2>

#### Base setup

Install required packages:

```bash
# With npm
npm i -D prettier @bokub/prettier-config

# With yarn
yarn add -D prettier @bokub/prettier-config
```

Add the config to your `package.json`:

```bash
npm pkg set prettier="@bokub/prettier-config"
```

#### _Optional:_ Setup pre-commit hook with husky & lint-staged

Install husky & lint-staged:

```bash
# With npm
npm i -D husky lint-staged

# With yarn
yarn add -D husky lint-staged
```

Setup git hook:

```bash
npx husky init
echo "npx lint-staged --concurrent false" > .husky/pre-commit
npm pkg set "lint-staged.*"="prettier --write --ignore-unknown"
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
    "prettier/prettier": "warn", // Optionally, you can set the error level to warn
  },
}
```

If you have a `lint-staged` configuration, add an ESLint task :

```bash
npm pkg set "lint-staged[*.{js,ts,vue}]"="eslint --fix"
```
