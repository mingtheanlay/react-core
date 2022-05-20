# Setting up ESLint and Prettier on ReactTS

---

## Vite installation

```bash
$ yarn create vite
```

## Choose tool

- Framework: react

- Variant: react-ts

## Install the dependency

```bash
$ yarn install
```

## Run development server

```bash
$ yarn dev
```

---

## Setting up ESLint

## Manual installation

<https://eslint.org/docs/user-guide/getting-started>

```bash
$ yarn add eslint --dev
```

Picking own configuaration

```bash
$ yarn create @eslint/config
```

Suggestion:

- To check syntax, find problem, and enforce code style

- JavaScript modules (import/export)

- React

- TypeScript (Yes)

- Browser

- Use popular style guide ([Airbnb](https://github.com/airbnb/javascript))

- JSON

- Install them now (Yes)

- Yarn

## AirBnb configuration

Using [AirBnb TypeScript](https://www.npmjs.com/package/eslint-config-airbnb-typescript)&#x20;

```bash
$ npm i eslint-config-airbnb-typescript
```

Go to `.eslintrc` and add `'airbnb-typescript'` to your project file if you are using TypeScript

.eslintrc additional plugin

```json
"plugin:@typescript-eslint/recommended",
"react-app/jest",
"prettier/@typescript-eslint",
"plugin:prettier/recommended",
"plugin:import/typescript",
"plugin:import/errors",
"plugin:import/warnings",
```

Add `"project": "./tsconfig.json"` to `parserOptionProject`

If you are using **Jest** for testing, include `env` with `"jest": true`, and include in `extents` with `"react-app/jest"`

Run ESLint to all file

```bash
$ npx eslint . --ext .js,.jsx,.ts,.tsx
```

Run ESLint to `/src` directory

```bash
$ npx eslint ./src
```

More command:&#x20;

<https://eslint.org/docs/user-guide/command-line-interface>

Or you can config lint command on **`package.json`**

Go to `script` in **`package.json`** and add (or you can eslint your preferable file)&#x20;

```json
"lint" : "eslint ./src"
or
"lint": "eslint --cache ./src"
```

If you prefer ESLint to fix the error

```json
"lint:fix" : "eslint --fix ./src"
```

## Config ESLint rule

Add Simple Sort Rule to **`plugins` by following this intruction:**

<https://github.com/lydell/eslint-plugin-simple-import-sort>

Default rules:

```json
 "plugins": ["react", "@typescript-eslint", "simple-import-sort"],
  "rules": {
    "react/function-component-definition": [2, { "namedComponents": "arrow-function" }],
    "react/react-in-jsx-scope": "off",
    "simple-import-sort/imports": "error",
    "simple-import-sort/exports": "error",
    "@typescript-eslint/comma-dangle": "off"
  }
```

More eslint rule:&#x20;

<https://eslint.org/docs/rules/>

## Install TailwindCSS

<https://tailwindcss.com/docs/guides/create-react-app>

## Config Prettier

Installation

<https://prettier.io/docs/en/install.html>

Config

<https://medium.com/how-to-react/config-eslint-and-prettier-in-visual-studio-code-for-react-js-development-97bb2236b31a>

<https://github.com/prettier/eslint-config-prettier>

### Prettier with TailwindCSS

<https://www.npmjs.com/package/prettier-plugin-tailwindcss>
