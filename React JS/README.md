# React JS Project Basic Setup

This Description contains the full guide to set up the initial `React JS` project using `create-react-app` on any Personal Computer.

[![React JS](https://img.shields.io/badge/React.js-61DAFB?style=for-the-badge&logo=React&logoColor=black)](#)
[![VSCode](https://img.shields.io/badge/Visual_Studio_Code-007ACC?style=for-the-badge&logo=visual%20studio%20code&logoColor=white)](#)
[![ESLint](https://img.shields.io/badge/ESLint-4B32C3?style=for-the-badge&logo=ESLint&logoColor=white)](#)

## Table of Contents

- [Editor Setup](#editor-setup)
  - [Plugins](#plugins)
  - [Settings](#settings)
  - [Set Line Breaks](#set-line-breaks)
- [React Project Setup](#react-project-setup)
  - [Create App](#create-app)
  - [Run App](#run-app)
- [Linting Setup](#linting-setup)
  - [Install Dev Dependencies](#install-dev-dependencies)
  - [Create Linting Configuration File Manually](#create-linting-configuration-file-manually)
  <!-- - [Solve Linting Conflict](#solve-linting-conflict) -->

## Editor Setup

Editor: VS Code (Visual Studio Code)

### Plugins

Install the below Plugins / Extensions in VS Code:

- ESLint
- Prettier - Code formatter

### Settings

Follow the below settings for VS Code -

1. Create a new folder called ".vscode" inside the React JS project root folder.
2. Create a new file called "settings.json" inside that folder.
3. Paste the below json in the newly created `settings.json` file and save the file.

```js
{
  // Theme - optional
  "workbench.colorTheme": "Community Material Theme Darker High Contrast",

  // Code Formatting Configuration
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
  "[javascript]": {
    "editor.formatOnSave": false,
    "editor.defaultFormatter": null
  },
  "[javascriptreact]": {
    "editor.formatOnSave": false,
    "editor.defaultFormatter": null
  },

  // Disables all built-in syntax checking
  "javascript.validate.enable": false,

  // Automatically fixes lint problems while saving a file
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true,
    "source.fixAll.tslint": true,
    "source.organizeImports": true
  },

  // Shows ESLint status in the Status Bar
  "eslint.alwaysShowStatus": true,

  // Emmets
  "emmet.triggerExpansionOnTab": true,
  "emmet.includeLanguages": {
    "javascript": "javascriptreact"
  }
}
```

### Set Line Breaks

Make sure in VS Code Editor, "LF" is selected as line feed instead of CRLF (Carriage return and line feed).
To do that, just click LF/CRLF in the bottom right corner of the `Status Bar` of the editor, click it, and change it to "LF". Else there would be errors in the setup.

<hr>

## React Project Setup

In order to create a react-based project, follow the instructions below.

### Create App

To create a new app, you may choose one of the following methods:

- npx

```sh
npx create-react-app my-app-name
```

- Yarn

```sh
yarn create react-app my-app-name
```

### Run App

To run the initial project structure (React App), follow the instructions below.

- npm

```sh
cd my-app-name
npm start
```

- Yarn

```sh
cd my-app-name
yarn start
```

<hr>

## Linting Setup

In order to lint and format the React project automatically according to the popular `airbnb` style guide, follow the instructions below.

### Install Dev Dependencies

**Multiple Commands:**

```sh
yarn add -D prettier
npx install-peerdeps --dev eslint-config-airbnb
yarn add -D eslint eslint-config-prettier eslint-plugin-prettier
yarn add -D eslint-plugin-react
```

**Single Command [Using Script]:**

_Copy-Paste this new script in the scripts section of the `package.json` file_

```json
 "lint": "npx install-peerdeps --dev eslint-config-airbnb && yarn add -D eslint prettier eslint-config-prettier eslint-plugin-prettier eslint-plugin-react"
```

and then simply run the below command in the terminal -

- Using Yarn:

```sh
yarn lint
```

- Using npm:

```sh
npm run lint
```

### Create Linting Configuration File Manually

Create a `.eslintrc.json` file in the project root and Copy-Paste the below contents:

```json
{
  "extends": [
    "airbnb",
    "airbnb/hooks",
    "eslint:recommended",
    "prettier",
    "plugin:jsx-a11y/recommended"
  ],
  "parserOptions": {
    "ecmaVersion": "latest",
    "sourceType": "module",
    "allowImportExportEverywhere": true
  },
  "env": {
    "browser": true,
    "node": true,
    "es6": true,
    "jest": true
  },
  "rules": {
    "react/react-in-jsx-scope": 0,
    "react-hooks/rules-of-hooks": "error",
    "no-console": 0,
    "react/state-in-constructor": 0,
    "indent": 0,
    "linebreak-style": 0,
    "react/prop-types": 0,
    "jsx-a11y/click-events-have-key-events": 0,
    "react/jsx-filename-extension": [
      1,
      {
        "extensions": [".js", ".jsx"]
      }
    ],
    "prettier/prettier": [
      "error",
      {
        "trailingComma": "es5",
        "singleQuote": true,
        "printWidth": 100,
        "tabWidth": 2,
        "semi": true,
        "endOfLine": "auto"
      }
    ]
  },
  "plugins": ["prettier", "react", "react-hooks"]
}
```

**Note:** _Now, this app can be run on the localhost by following [Run App](#run-app) instructions but if there any error arrives, most probably it will be generated because of the `eslint`, try to lint all the files by saving each them or solve the errors by following the given error reports on the terminal!_

<!---
### Solve Linting Conflict

After doing all these steps, there would occur a conflict between ".eslintrc.json" and "BaseConfig" due to version differences.

`ERROR in [eslint] Plugin "react" was conflicted between ".eslintrc" and "BaseConfig .....`

To solve this, create a file named, `.env` in the `my-app-name` folder and paste the below code:

```env
SKIP_PREFLIGHT_CHECK = true
```
-->
