# VS Code Global Level User Setting [setting.json] #
[![VSCode](https://img.shields.io/badge/Visual_Studio_Code-007ACC?style=for-the-badge&logo=visual%20studio%20code&logoColor=white)](#)

### Steps to follow

1. Open VS Code
2. Go to Settings Or, press `Ctrl + ,`
3. Click on the 3rd Icon from Top Right Side, named: `Open Settings (JSON)`
4. Copy-Paste the below code
5. Optional Font Installation: `FIRA CODE` (needs to installed to use)

```js
// Shibam Saha
// VS Code - User Settings [settings.json]

/*
  Required Extensions:

  Auto Close Tag
  Auto Rename Tag
  Better Comments
  C/C++ Extension pack
  Code Runner
  Code Spell Checker
  Colorize
  Community Material theme
  Console Ninja
  Css Peek
  Dracula Official [Theme]
  Error Lens
  ES7+ React/Redux/React-Native Snippets
  ESLint
  Extension Pack for Java
  Highlight Matching Tag
  HTML End Tag Labels
  Intellicode
  JavaScript (ES6) Code Snippets
  Live Server
  Material Icon Theme / vscode-icons
  Path Intellisense
  Postman
  Prettier - Code Formatter
  Quokka.js
  Snipped
  Tabnine AI
  Tailwind CSS IntelliSense
  Turbo Console Log
  vscode-pdf
*/

{
  // Editor
  "editor.fontSize": 16,
  "editor.wordWrap": "on",
  "editor.formatOnSave": true,
  "editor.mouseWheelZoom": true,
  "editor.minimap.enabled": true,
  "editor.minimap.showSlider": "always",
  "editor.minimap.maxColumn": 30,
  "editor.fontLigatures": true,
  "editor.suggestSelection": "first",
  "editor.tabCompletion": "on",
  "editor.acceptSuggestionOnEnter": "smart",
  "editor.accessibilitySupport": "off",
  "editor.guides.bracketPairs": true,
  "editor.bracketPairColorization.enabled": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.fontFamily": "Fira Code, Consolas, Courier New, monospace",
  "editor.quickSuggestions": {
    "strings": true
  },
  "editor.tokenColorCustomizations": {
    "textMateRules": [
      {
        "scope": "comment",
        "settings": {
          "fontStyle": "italic",
          "foreground": "#999999"
        }
      }
    ]
  },

  // Editor Cursor
  "editor.cursorBlinking": "expand",
  "editor.cursorSmoothCaretAnimation": "on",

  //  Debug Console
  "debug.console.fontSize": 16,

  // File Explorer
  "explorer.confirmDragAndDrop": false,

  // Terminal
  "terminal.integrated.fontSize": 16,
  "terminal.integrated.cursorStyle": "line",
  "terminal.integrated.fontWeight": "normal",
  "terminal.integrated.cursorBlinking": true,
  "terminal.integrated.fontFamily": "Fira Code, Consolas",

  // Work Bench
  "workbench.iconTheme": "material-icon-theme",
  "workbench.colorTheme": "Community Material Theme Darker High Contrast",
  "workbench.editor.untitled.hint": "hidden",
  "workbench.colorCustomizations": {
    "editorCursor.foreground": "#ffff00",
    "terminalCursor.foreground": "#ffff00"
  },

  // Files Auto Save
  "files.autoSaveDelay": 500,
  "files.autoSave": "afterDelay",

  // Code Runner [Extension Settings]
  "code-runner.runInTerminal": true,
  "code-runner.saveFileBeforeRun": true,
  "code-runner.clearPreviousOutput": true,

  // Live Server [Extension Settings]
  "liveServer.settings.root": "/",
  "liveServer.settings.donotShowInfoMsg": true,

  // Prettier [Extension Settings]
  "prettier.singleQuote": true,

  // Snipped (Screenshot) [Extension Settings]
  "snipped.enablePng": true,

  // Better Comments [Extension Settings]
  "better-comments.tags": [
    {
      "tag": "?",
      "color": "#FF2D00", // ? Red
      "strikethrough": false,
      "underline": false,
      "backgroundColor": "transparent",
      "bold": false,
      "italic": false
    },
    {
      "tag": "!",
      "color": "#3498DB", // ! Blue
      "strikethrough": false,
      "underline": false,
      "backgroundColor": "transparent",
      "bold": false,
      "italic": false
    },
    {
      "tag": "#",
      "color": "#ffffff", // # White
      "strikethrough": false,
      "underline": false,
      "backgroundColor": "transparent",
      "bold": false,
      "italic": false
    },
    {
      "tag": "-",
      "color": "#FF8C00", // - Orange
      "strikethrough": false,
      "underline": false,
      "backgroundColor": "transparent",
      "bold": false,
      "italic": false
    },
    {
      "tag": "*",
      "color": "#FFD700", // * Golden
      "strikethrough": false,
      "underline": false,
      "backgroundColor": "transparent",
      "bold": false,
      "italic": false
    },

    {
      "tag": "^",
      "color": "#FF1493", // ^ Pink
      "strikethrough": false,
      "underline": false,
      "backgroundColor": "transparent",
      "bold": false,
      "italic": false
    }
  ],

  // Colorize [Extension Settings]
  "colorize.languages": ["html", "css", "javascript", "javascriptreact"],

  // Tailwind CSS
  "tailwindCSS.emmetCompletions": true,
  "tailwindCSS.includeLanguages": {
    "html": "html",
    "css": "css",
    "javascript": "javascript"
  },
  "tailwindCSS.hovers": true,

  "C_Cpp.files.exclude": {
    "**/.vscode": true,
    "**/.vs": true
  },

  // Error Lens
  "errorLens.followCursor": "activeLine",
  "errorLens.followCursorMore": -1, // Stops showing error statements in the editor

  // Code Formatting
  // "[javascript]": {
  //   "editor.formatOnSave": false,
  //   "editor.defaultFormatter": null
  // },
  // "[javascriptreact]": {
  //   "editor.formatOnSave": false,
  //   "editor.defaultFormatter": null
  // },
  // "editor.codeActionsOnSave": {
  //   "source.fixAll.eslint": true,
  //   "source.fixAll.tslint": true,
  //   "source.organizeImports": true
  // },

  // C++ Intellisense [Extension Settings]

  "vsintellicode.modify.editor.suggestSelection": "automaticallyOverrodeDefaultValue",

  // File Exclusion
  "files.exclude": {
    "**/.classpath": true,
    "**/.factorypath": true,
    "**/.git": false,
    "**/.project": true,
    "**/.settings": true
  },

  // Code Formatting for C++
  "[cpp]": {
    "editor.wordBasedSuggestions": false,
    "editor.suggest.insertMode": "replace",
    "editor.semanticHighlighting.enabled": true,
    "editor.defaultFormatter": "ms-vscode.cpptools"
  },

  "css.lint.unknownAtRules": "ignore",
  "[python]": {
    "editor.formatOnType": true
  },
  "prettier.jsxSingleQuote": true,
  "prettier.trailingComma": "none",
  "tabnine.experimentalAutoImports": true,
  "terminal.integrated.env.windows": {}
}
```
