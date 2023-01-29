# VS Code Global Level User Setting [setting.json]

```
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
  Community Material theme
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
  Path Intellisense
  Prettier - Code Formatter
  Quokka.js
  Snipped
  Tailwind CSS IntelliSense
  Turbo Console Log
  vscode-icons
  vscode-pdf
*/

{
  // Editor
  "editor.fontSize": 16,
  "editor.wordWrap": "on",
  "editor.formatOnSave": true,
  "editor.mouseWheelZoom": true,
  "editor.minimap.enabled": false,
  // "editor.minimap.size": "fill",
  // "editor.minimap.showSlider": "always",
  "editor.fontLigatures": true,
  "editor.suggestSelection": "first",
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
  "editor.cursorSmoothCaretAnimation": true,

  //  Debug Console
  "debug.console.fontSize": 16,

  // Terminal
  "terminal.integrated.fontSize": 16,
  "terminal.integrated.cursorStyle": "line",
  "terminal.integrated.fontWeight": "normal",
  "terminal.integrated.cursorBlinking": true,
  "terminal.integrated.fontFamily": "Fira Code, Consolas",

  // Work Bench
  "workbench.iconTheme": "vscode-icons",
  "workbench.colorTheme": "Default Dark+",
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

  // Snipped (Screenshot) [Extension Settings]
  "snipped.enablePng": true,

  // Better Comments [Extension Settings]
  "better-comments.tags": [
    {
      "tag": "!",
      "color": "#FF2D00", // !Red
      "strikethrough": false,
      "underline": false,
      "backgroundColor": "transparent",
      "bold": false,
      "italic": false
    },
    {
      "tag": "?",
      "color": "#3498DB", // ?Blue
      "strikethrough": false,
      "underline": false,
      "backgroundColor": "transparent",
      "bold": false,
      "italic": false
    },
    {
      "tag": "//",
      "color": "#ffffff", // //White
      "strikethrough": true,
      "underline": false,
      "backgroundColor": "transparent",
      "bold": false,
      "italic": false
    },
    {
      "tag": "todo",
      "color": "#FF8C00", // todo Orange
      "strikethrough": false,
      "underline": false,
      "backgroundColor": "transparent",
      "bold": false,
      "italic": false
    },
    {
      "tag": "*",
      "color": "#FFD700", // *Golden
      "strikethrough": false,
      "underline": false,
      "backgroundColor": "transparent",
      "bold": false,
      "italic": false
    },

    {
      "tag": "^",
      "color": "#FF1493", // ^Pink
      "strikethrough": false,
      "underline": false,
      "backgroundColor": "transparent",
      "bold": false,
      "italic": false
    }
  ],

  // Code Spell Checker [Extension Settings]
  "cSpell.userWords": [
    "SHIBAM",
    "vsintellicode",
    // Add More Words 
  ],

  // Tailwind CSS
  "tailwindCSS.emmetCompletions": true,
  "tailwindCSS.includeLanguages": {
    "html": "html",
    "javascript": "javascript",
    "css": "css"
  },

  "C_Cpp.files.exclude": {
    "**/.vscode": true,
    "**/.vs": true
  },

  // Error Lens
  "errorLens.followCursor": "activeLine",
  "errorLens.followCursorMore": -1, // Stops showing error statements in the editor

  // Code Formatting
  "[javascript]": {
    "editor.formatOnSave": false,
    "editor.defaultFormatter": null
  },
  "[javascriptreact]": {
    "editor.formatOnSave": false,
    "editor.defaultFormatter": null
  },
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true,
    "source.fixAll.tslint": true,
    "source.organizeImports": true
  },

  // ESLint [Extension Settings]
  "eslint.alwaysShowStatus": true,

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

  "css.lint.unknownAtRules": "ignore"
}
```
