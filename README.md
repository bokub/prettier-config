# @bokub / prettier-config

> My personal [Prettier](https://prettier.io) config.

## Usage

**Install**:

```bash
# Just the config
npm i -D @bokub/prettier-config

# Whole package
npm i -D prettier pretty-quick husky @bokub/prettier-config
```

**Add the following to your `package.json`**:

```jsonc
{
    "scripts": {
        "pretty-quick": "pretty-quick"
    },
    "husky": {
        "hooks": {
            "pre-commit": "pretty-quick --staged"
        }
    },
    "prettier": "@bokub/prettier-config"
}
```
