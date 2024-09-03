# @pasifer/eslint-config
AdonisJS's [eslint-config](https://github.com/adonisjs/eslint-config) was used as the base for this package and modified for Parsifer's use. If you're working with Parsifer's services, we recommend you check out their packages.

## Installation

Install the package from the npm registry.

```sh
npm i -D @parsifer/eslint-config

# Install peer dependencies
npm i -D eslint@9 prettier@3
```

## Usage

After installation, use one of the following presets depending on the nature of your application/library.

**For AdonisJS App development**: Use the following preset when developing an AdonisJS application

```ts
// eslint.config.js
import { configApp } from '@parsifer/eslint-config'
export default configApp()
```

**For package or library development**: Use the following preset when developing a package

```ts
// eslint.config.js
import { config } from '@parsifer/eslint-config'
export default config()
```

## Adding additional config blocks

You can pass additional config blocks as multiple arguments to one of the preset functions.

```ts
import { configApp, INCLUDE_LIST, IGNORE_LIST } from '@parsifer/eslint-config'

export default configApp({
  name: 'Custom config',
  files: INCLUDE_LIST,
  ignores: IGNORE_LIST,
  plugins: {
    // ESLint plugins go here
  },
  rules: {
    // ESLint rules go here
  },
})
```