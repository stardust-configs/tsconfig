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
<summary>Node.js v16</summary>

```jsonc
{
  "extends": "@stardust-configs/tsconfig/node16.json"
}
```

</details>

<details>
<summary>Next.js</summary>

```jsonc
{
  "extends": "@stardust-configs/tsconfig/next.json",
  "include": ["next-env.d.ts", "**/*.ts", "**/*.tsx"],
  "exclude": ["node_modules"]
}
```

</details>

## Override

Override `tsconfig.json`.

<details>
<summary><code>baseUrl</code></summary>

```jsonc
{
  "extends": "@stardust-configs/tsconfig",
  "compilerOptions": {
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
      "@bar/*": ["./src/bar/*"],
      "@baz/*": ["./src/baz/*"]
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
<summary><code>outDir</code></summary>

```jsonc
{
  "extends": "@stardust-configs/tsconfig",
  "compilerOptions": {
    "outDir": "./dist"
  }
}
```

</details>

<details>
<summary><code>noEmit</code></summary>

```jsonc
{
  "extends": "@stardust-configs/tsconfig",
  "compilerOptions": {
    "noEmit": true
  }
}
```

</details>

<details>
<summary><code>plugins</code></summary>

```jsonc
{
  "extends": "@stardust-configs/tsconfig",
  "compilerOptions": {
    "plugins": [{ "name": "foo" }, { "name": "bar" }, { "name": "baz" }]
  }
}
```

</details>

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
