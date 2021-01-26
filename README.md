# @stardust-configs/tsconfig

> Shareable TypeScript config

## Install

```bash
$ npm install @stardust-configs/tsconfig --save-dev
```

## Usage

Edit `tsconfig.json`.

<details>
<summary>Default</summary>

```jsonc
{
  "extends": "@stardust-configs/tsconfig"
}
```

</details>

<details>
<summary>Recommended</summary>

```jsonc
{
  "extends": "@stardust-configs/tsconfig/recommended.json"
}
```

</details>

<details>
<summary>Node.js v12</summary>

```jsonc
{
  "extends": "@stardust-configs/tsconfig/node12.json"
}
```

</details>

<details>
<summary>Node.js v14</summary>

```jsonc
{
  "extends": "@stardust-configs/tsconfig/node14.json"
}
```

</details>

<details>
<summary>Next.js</summary>

```jsonc
{
  "extends": "@stardust-configs/tsconfig/next.json"
}
```

</details>

## Override

Override `tsconfig.json`.

<details>
<summary><code>declaration</code></summary>

```jsonc
{
  "extends": "@stardust-configs/tsconfig",
  "compilerOptions": {
    "declaration": true
  }
}
```

</details>

<details>
<summary><code>outDir</code> & <code>baseUrl</code></summary>

```jsonc
{
  "extends": "@stardust-configs/tsconfig",
  "compilerOptions": {
    "outDir": "./dist",
    "baseUrl": "./"
  }
}
```

</details>

<details>
<summary><code>paths</code></summary>

```jsonc
{
  "extends": "@stardust-configs/tsconfig",
  "compilerOptions": {
    "paths": {
      "@foo/*": ["./src/foo/*"],
      "@bar/*": ["./src/bar/*"]
    }
  }
}
```

</details>

<details>
<summary><code>typeRoots</code></summary>

```jsonc
{
  "extends": "@stardust-configs/tsconfig",
  "compilerOptions": {
    "typeRoots": ["./node_modules/@types", "./src/@types"]
  }
}
```

</details>

<details>
<summary><code>experimentalDecorators</code> & <code>emitDecoratorMetadata</code></summary>

```jsonc
{
  "extends": "@stardust-configs/tsconfig",
  "compilerOptions": {
    "experimentalDecorators": true,
    "emitDecoratorMetadata": true
  }
}
```

</details>

## Publish a new version

```bash
# Write token to .env file
$ echo "CONVENTIONAL_GITHUB_RELEASER_TOKEN=\"[GITHUB_TOKEN]\"" > .env

# Bump version
$ yarn run version

# Push to GitHub
$ git push --follow-tags origin master

# Create a new release
$ yarn release

# Publish to npm
$ npm publish
```

## FAQ

### How decided `target` of `nodexx.json`?

Reference [Node Target Mapping · microsoft/TypeScript Wiki](https://github.com/microsoft/TypeScript/wiki/Node-Target-Mapping).

### Why `compilerOptions` contains uppercase letters?

I know that developers are generally written in lowercase only. However, [JSON Schema](https://json.schemastore.org/tsconfig) contains uppercase letters.

## Author

[@p-chan](https://github.com/p-chan)

## License

MIT

---

Inspired by [sindresorhus/tsconfig](https://github.com/sindresorhus/tsconfig)
