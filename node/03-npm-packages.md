# NPM Projects
To use NPM capabilities in your project you need to make directory a NPM Project. NPM Project - directory containing:
* `package.json` - main file for NPM project. Commit this to Git.
* `node_modules` (will be created after first package install) - all packages will be installed here. Do not commit to Git.
* `package-lock.json` (will be created after first package install) - locks Package versions. Commit this to Git. 

**Create Project**

* `npm init` - will ask many questions (press Enter to skip) and create new project in current directory. `npm init -y` to skip questions.


# NPM Packages (libraries)

## Project Packages
Packages that are available only inside project directory.

**Install Package**

Look for packages at [npmjs](https://www.npmjs.com/). Contains package description, short documentation.

* `npm install lodash` - install package. Package will be stored to node_modules directory and also saved in package.json and package-lock.json files.
* `npm uninstall lodash` - uninstall package.
* `npm install` - install all packages saved in package.json and package-lock.json files. E.g. after you deleted node_modules folder or downloaded project.


**Use in your code**

`npm install lodash` - install lodash library.

`index.js` file uses "lodash" library:
```
// Load package to "_" variable (use package name in require)
const _ = require('lodash');

// Use package
_.isString('text');
```

## Global Packages (Tools)
Tool packages that you can run from anywhere in Terminal.

`npm install mocha -g` - instal "mocha" test runner `-g` for "global".

`mocha` - run tool package from anywhere in Terminal.


