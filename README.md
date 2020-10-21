# eslint-config-mingelz

[![Version](https://img.shields.io/npm/v/eslint-config-mingelz.svg?style=flat)](https://www.npmjs.com/package/eslint-config-mingelz)

A shared [ESLint](https://eslint.org) configuration with Chinese comments by mingelz.

一份带有完整中文注释的 ESLint 规则。请打开 [rules](./rules) 目录下的文件，阅读每个规则的详细说明。

---

* [Quick start](#quick-start)
  * [Installation](#installation)
  * [Configure](#configure)
* [Documentation](#documentation)
  * [Basic configuration](#basic-configuration)
  * [Vue configuration](#vue-configuration)
  * [React configuration](#react-configuration)
  * [Node.js configuration](#nodejs-configuration)
  * [ES Module configuration](#es-module-configuration)
  * [JSDoc configuration](#jsdoc-configuration)
  * [*[WIP]* JSX accessibility configuration](#wip-jsx-accessibility-configuration)

## Quick start

### Installation

```sh
npm install eslint-config-mingelz --save-dev
```

### Configure

Add a `.eslintrc.js` file with following content to your project root directory:

```js
module.exports = {
  env: {
    browser: true,
    node: true,
  },
  extends: [
    'mingelz',
  ],
}
```

## Documentation

### Basic configuration

**NOTICE**:
This configuration is dependent on [eslint](https://eslint.org)@^7.11,
please install it manully: `npm install -D eslint`.

```js
module.exports = {
  env: {
    browser: true,
    node: true,
  },
  extends: [
    'mingelz',
  ],
  rules: {
    // your special rules
  },
}
```

### Vue configuration

**NOTICE**:
This configuration is dependent on [eslint-plugin-vue](https://github.com/vuejs/eslint-plugin-vue)@^7.1,
please install it manully: `npm install -D eslint-plugin-vue`

```js
module.exports = {
  // ...
  extends: [
    'mingelz',
    // The configuration will detect Vue.js version of your project automatic.
    'mingelz/rules/vue',
  ],
  // ...
}
```

### React configuration

**NOTICE**:
This configuration is dependent on [eslint-plugin-react](https://github.com/yannickcr/eslint-plugin-react)@^7.21,
please install it manully: `npm install -D eslint-plugin-react`

```js
module.exports = {
  // ...
  extends: [
    'mingelz',
    'mingelz/rules/react',
  ],
  // ...
}
```

### Node.js configuration

[The ESLint built-in Node.js/CommonJS-specific rules are deprecating](https://eslint.org/blog/2020/02/whats-coming-in-eslint-7.0.0#deprecating-node-js-commonjs-specific-rules), use *eslint-plugin-node* instead.

**NOTICE**:
This configuration is dependent on [eslint-plugin-node](https://github.com/mysticatea/eslint-plugin-node)@^11.1,
please install it manully: `npm install -D eslint-plugin-node`

```js
module.exports = {
  // ...
  extends: [
    'mingelz',
    'mingelz/rules/node',
  ],
  // ...
}
```

### ES Module configuration

**NOTICE**:
This configuration is dependent on [eslint-plugin-import](https://github.com/benmosher/eslint-plugin-import)@^2.22,
please install it manully: `npm install -D eslint-plugin-import`

If you are using Webpack [resolve.alias](https://webpack.js.org/configuration/resolve/#resolvealias),
it is recommended to install [eslint-import-resolver-webpack](https://www.npmjs.com/package/eslint-import-resolver-webpack) via `npm install -D eslint-import-resolver-webpack`,
and configure it according to the webpack configuration file.

```js
module.exports = {
  // ...
  extends: [
    'mingelz',
    'mingelz/rules/es-module',
  ],
  // webpack config example
  settings: {
    'import/resolver': {
      webpack: {
        config: './webpack.config.js',
      },
    },
  },
  // ...
}
```

### JSDoc configuration

[The ESLint built-in JSDoc rules was deprecated](https://eslint.org/blog/2018/11/jsdoc-end-of-life), use *eslint-plugin-jsdoc* instead.

**NOTICE**:
This configuration is dependent on [eslint-plugin-jsdoc](https://github.com/gajus/eslint-plugin-jsdoc)@30.7,
please install it manully: `npm install -D eslint-plugin-jsdoc`

```js
module.exports = {
  // ...
  extends: [
    'mingelz',
    'mingelz/rules/jsdoc',
  ],
  // ...
}
```

### *[WIP]* JSX accessibility configuration

**NOTICE**:
This configuration is dependent on [eslint-plugin-jsx-a11y](https://github.com/evcohen/eslint-plugin-jsx-a11y),
please install it manully: `npm install -D eslint-plugin-jsx-a11y`

```js
module.exports = {
  // ...
  extends: [
    'mingelz',
    'mingelz/rules/jsx-a11y',
  ],
  // ...
}
```
