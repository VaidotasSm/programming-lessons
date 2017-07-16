# NPM Scripts

## Overview
`package.json` contains special element called "scripts". Scripts are custom scripts that will get executed by running `npm run xxx` where xxx is script name.

**Example run application**

Instead of manually running `node index.js` in terminal, you can:
```
"scripts": {
    "start": "node index.js"
},
```
`npm run start` - execute script.

## Use Tool Packages

This is similar to Global Packages, but only for this directory. You can use all locally installed packages as you would use global packages inside `"scripts"` of `package.json`.

**Example**

`npm install mocha --save-dev` - install test runner. For most tools it's recommended to install with `--save-dev` to separate code dependencies and development tool dependencies, but emitting it would still work.

`package.json` - find "scripts" and add one line - command `mocha` runs tests inside ./test folder:

```
"scripts": {
    "test": "mocha"
},
```

`npm run test` - run "test" script





