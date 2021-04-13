# @bokub / prettier-config

[![Code style][style-src]][style-href]
[![Downloads][downloads-src]][downloads-href]

> My personal [Prettier](https://prettier.io) config / workflow

#### Install

```bash
npm i -D prettier @bokub/prettier-config
```

#### Add the following to your `package.json`:

```json
{
  "prettier": "@bokub/prettier-config"
}
```

#### _Optional:_ Setup pre-commit hook

```bash
npx husky-init
npm i -D pretty-quick
npx husky set .husky/pre-commit "npx pretty-quick --staged"
```

#### _Optional:_ Run prettier on old code

```bash
npx prettier --write .
```

[style-src]: https://flat.badgen.net/badge/code%20style/prettier/ff69b4
[style-href]: https://github.com/prettier/prettier
[downloads-src]: https://flat.badgen.net/npm/dt/@bokub/prettier-config
[downloads-href]: https://www.npmjs.com/package/@bokub/prettier-config
