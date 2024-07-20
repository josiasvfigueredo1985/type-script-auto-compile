# TypeScript - Easy Beginning Tutorial

***To read this with better formatting, right-click on the file in Explorer, choose "Open With", then select "Markdown Preview".***

This is a small project aimed at demonstrating how to start coding with TypeScript without worrying about compiling it each time you need to run your code. TypeScript is awesome, but the fact that we need to compile it to JavaScript can be annoying, especially for beginners. So, here are a few tips to help you start coding!

## Table of Contents
1. [Required](#required)
2. [VS Code and Extensions](#vs-code-and-extensions)
3. [Prepare Your Local Repo](#prepare-your-local-repo)
4. [Install TypeScript on Your Repo](#install-typescript-on-your-repo)
5. [Update tsconfig.json File](#update-tsconfigjson-file)
6. [NPM Configuration](#npm-configuration)
7. [Create Your First TypeScript Code](#create-your-first-typescript-code)
8. [Configure Auto Compile and Run Current File Code](#configure-auto-compile-and-run-current-file-code)
9. [Run Your Code](#run-your-code)
10. [Update Your Code and Run It Again](#update-your-code-and-run-it-again)
11. [Optionals](#optionals)

### Required
- [Node.js](https://nodejs.org/en/download/current)
- [TypeScript](https://www.typescriptlang.org/download)
- [Git](https://git-scm.com/downloads)

### VS Code and extensions
 VS Code is mandatory but extensions are optional but highly recommended

- [VS Code](https://code.visualstudio.com/)
- [Material Icon](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)
- [TypeScript](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-typescript-next)
- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [Dracula Pure](https://marketplace.visualstudio.com/items?itemName=blackblackcat.dracula-pure)
- [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
- [TabNine](https://marketplace.visualstudio.com/items?itemName=TabNine.tabnine-vscode)
- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)

### Prepare Your Local Repo
- Create a new folder
- Open New Terminal on VS Code
- Command: `git init`
- Create `.gitignore` file
- Create `README.md` file
- Open Source Control on VS Code and commit your changes
- Publish your branch
- Create a branch from master (Optional)

### Install TypeScript on Your Repo
- Command 1: `npm install -g typescript`
- Command 2: `tsc --init` (tsconfig.json will be added automatically to your project folder, no need to modify for now)

### Update tsconfig.json File
- Change line to `"outDir": "./output",`
- Uncomment `sourceMap` line

### NPM Configuration
- Command: `npm init`
- Open `package.json` file that was created on the step before and add the following line inside "scripts": `"build": "tsc"`

### Create Your First TypeScript Code
- Add a `src` folder
- Add an `output` folder
- Add `<nameYouWant>.ts` file into `src` folder
- Add the following code to it:
    ```typescript
    class MyFirstCode {
        name: string;
        age: number;
        constructor(name: string, age: number) {
            this.name = name;
            this.age = age;
        }
    }
    
    class Greetings extends MyFirstCode {
        greet() {
            console.log(`Hello ${this.name}! Congrats! Your age is ${this.age}!`);
        }
    }
    
    const person = new Greetings("John", 25);
    person.greet();
    ```

### Configure Auto Compile and Run Current File Code
- Open `RUN AND DEBUG` menu on VS Code
- Select `create a launch.json file`
- Select `Node.js` option
- Add the following lines inside configurations:
    ```json
    "preLaunchTask": "npm: build",
    "console": "integratedTerminal",
    ```
- Modify line to `"program": "${file}",`

### Run Your Code
- Press `F5` and see the magic happens!🧙‍♂️
    - JavaScript files should be created into `output` folder
    - Terminal should open with compiling status
    - After compiling, TypeScript code should run successfully

### Update Your Code and Run It Again
- It should update and run automatically according to your changes 🤖

### Optionals
- Add `output` folder to .gitignore
- Commit your changes to your repository
- Check out your GitHub repository
- Always commit your changes and follow it with GitLens
- Add ESLint integration to your project (Google it)
- Add Husky integration and pre-commit configurations (Google it)

**❤️💻HAPPY CODING!!!💻❤️**
