---
layout: default
title: Prettier and Eslint
parent: JavaScript & TypeScript
nav_order: 1
---

# Prettier and Eslint configurations

In dpstudio we use prettier and eslint to format our codebase cohesively.

## Configuration

### The options for prettier are:

```javascript
module.exports = {
  tabWidth: 2,
  semi: true,
  singleQuote: true,
};
```

### While the rules for eslint are:

```json
rules: {
    'no-param-reassign': 'off',

    'import/first': 'off',
    'import/named': 'error',
    'import/namespace': 'error',
    'import/default': 'error',
    'import/export': 'error',
    'import/extensions': 'off',
    'import/no-unresolved': 'off',
    'import/no-extraneous-dependencies': 'off',
    'import/prefer-default-export': 'off',
    'prefer-promise-reject-errors': 'off',

    // TypeScript
    quotes: ['error', 'single', { avoidEscape: true }],
    '@typescript-eslint/explicit-function-return-type': 'off',
    '@typescript-eslint/explicit-module-boundary-types': 'off',

    // allow debugger during development only
    'no-debugger': process.env.NODE_ENV === 'production' ? 'error' : 'off',

    // allow consule during development only
    'no-console': process.env.NODE_ENV === 'production' ? 'warn' : 'off',

  }
```

### Plugins

For Vue projects we also extend the following:

- 'plugin:vue/essential', // Priority A: Essential (Error Prevention)
- 'plugin:vue/strongly-recommended', // Priority B: Strongly Recommended (Improving Readability)
- 'airbnb-base',
- 'prettier',
- 'prettier/vue',
- 'prettier/@typescript-eslint',
- 'plugin:prettier/recommended',

## IDE integrations

In IntelliJ, to automatically run prettier at each file save:
1. Install the Prettier plugin
1. Install the File Watcher plugin
1. Go to settings, Languages & Frameworks, JavaScript, check Run on save for files
1. Use `{**/*,*}.{js,ts,jsx,tsx,vue}` as pattern 

## Run via CLI

You can run prettier and eslint fix via cli for the whole project using:

`prettier -w <folder>; eslint --ext .js,.ts,.vue --ignore-path .gitignore <folder> --fix`

e.g. `prettier -w src; eslint --ext .js,.ts,.vue --ignore-path .gitignore ./src --fix`

###### *Author: Roberto Cabassi Bombardieri*
