---
title: My Editor Setup
---

<Intro>

A properly configured editor can make code clearer to read and faster to write. It can even help you catch bugs as you write them!

</Intro>

<YouWillLearn>

* What the most popular editors are
* How to format your code automatically

</YouWillLearn>

## Your editor {/*your-editor*/}

[VS Code](https://code.visualstudio.com/) is one of the most popular editors in use today.

## Recommended text editor features {/*recommended-text-editor-features*/}

### Linting {/*linting*/}

Code linters find problems in your code as you write, helping you fix them early.  

* [ESLint](https://eslint.org/) is a popular, open source linter for JavaScript. 
* [Install ESLint with the recommended configuration for React](https://www.npmjs.com/package/eslint-config-react-app) (be sure you have [Node installed!](https://nodejs.org/en/download/current/))
* [Integrate ESLint in VSCode with the official extension](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

**Make sure that you've enabled all the [`eslint-plugin-react-hooks`](https://www.npmjs.com/package/eslint-plugin-react-hooks) rules for your project.** They are essential and catch the most severe bugs early.  

The recommended [`eslint-config-react-app`](https://www.npmjs.com/package/eslint-config-react-app) **preset** already includes them.

### Formatting {/*formatting*/}

[Prettier](https://prettier.io/) clean up your code by reformatting it to conform to preset, configurable rules.

- install the [Prettier extension in VSCode](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

#### Formatting on save {/*formatting-on-save*/}

Ideally, you should format your code on every save. VS Code has settings for this!

1. In VS Code, press `CTRL/CMD + SHIFT + P`.
2. Type "settings"
3. Hit Enter
4. In the search bar, type "format on save"
5. Be sure the "format on save" option is ticked!

> If your ESLint preset has formatting rules, they may conflict with Prettier.  
> - We recommend disabling all formatting rules in your ESLint preset using [`eslint-config-prettier`](https://github.com/prettier/eslint-config-prettier) so that ESLint is *only* used for catching logical mistakes. 
> 
> If you want to enforce that files are formatted before a pull request is merged, 
> - use [`prettier --check`](https://prettier.io/docs/en/cli.html#--check) for your continuous integration.
