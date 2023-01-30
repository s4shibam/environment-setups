# React JS Project Basic Setup #

This Description contains the full guide to setup initial `React JS` project using `create-react-app` in any Personal Computer.

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
  - [Create Linting Configuration file manually](#create-linting-configuration-file-manually)
  - [Solve Linting Conflict](#solve-linting-conflict)


## Editor Setup

  Editor: VS Code (Visual Studio Code)
  
### Plugins

Install the below plugins:

- ESLint
- Prettier - Code formatter

### Settings

Follow the below settings for VS Code -

1. Create a new folder called ".vscode" inside the React JS project folder (Setting will be applicable for all Reach.JS projects).
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
  "javascript.validate.enable": false, // Disables all built-in syntax checking
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true,
    "source.fixAll.tslint": true,
    "source.organizeImports": true
  },
  "eslint.alwaysShowStatus": true,
  
  // Emmet
  "emmet.triggerExpansionOnTab": true,
  "emmet.includeLanguages": {
    "javascript": "javascriptreact"
  }
}
```

### Set Line Breaks

Make sure in VS Code Editor, "LF" is selected as line feed instead of CRLF (Carriage return and line feed).
To do that, just click LF/CRLF in bottom right corner `Status Bar` of editor, click it and change it to "LF". Else there would be errors in the setup.

<hr>

## React Project Setup

In order to create a react based project, follow the instructions below.

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
To run the initial project structure (React App),  follow the instructions below.

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

In order to lint and format the React project automatically according to popular `airbnb` style guide, follow the instructions below.

### Install Dev Dependencies

**Multiple Commands:**

```sh
yarn add -D prettier
yarn add -D babel-eslint
npx install-peerdeps --dev eslint-config-airbnb
yarn add -D eslint-config-prettier eslint-plugin-prettier
```


**Single Command [Using Script]:**

_Copy-Paste this new script in the scripts section of `package.json` file_

```json
  "lint": "yarn add -D prettier && yarn add -D babel-eslint && npx install-peerdeps --dev eslint-config-airbnb && yarn add -D eslint-config-prettier eslint-plugin-prettier"
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

```js
{
  "extends": [
    "airbnb",
    "airbnb/hooks",
    "eslint:recommended",
    "prettier",
    "plugin:jsx-a11y/recommended"
  ],
  "parser": "babel-eslint",
  "parserOptions": {
    "ecmaVersion": 8
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
        "tabWidth": 4,
        "semi": true,
        "endOfLine": "auto"
      }
    ]
  },
  "plugins": ["prettier", "react", "react-hooks"]
}
```

### Solve Linting Conflict

After doing all these steps, there would occur a conflict between ".eslintrc.json" and "BaseConfig" due to version differences.

`ERROR in [eslint] Plugin "react" was conflicted between ".eslintrc" and "BaseConfig .....`

To solve this, create a file named, `.env` in `my-app-name` folder and paste the below code:

```env
SKIP_PREFLIGHT_CHECK = true
```

