# Node.js (version 8+) introduction

## Overview (primitive)
* Node - basically a tool to run JavaScript files outside of browser.
* NPM (Node Package Manager) - tool to manage Node packages (libraries) and your projects. Comes with Node.js installation.

## Install
* Manual
* Windows Chocolatey: `choco install nodejs.install -y`
* Mac Homebrew: `brew install node`
* Check if installed correctly - run commands to check versions of Node and NPM:
  * `node --version`
  * `npm --version`

# NPM (Node Package Manager)

## NPM Projects

**Create Project**

* `npm init` - will ask many questions (press Enter to skip) and create new project in current directory. `npm init -y` to skip questions.
* Directory structure:
  * `package.json` - main file for NPM project. Commit this to Git.
  * `node_modules` (will be created after first package install) - all packages will be installed here. Do not commit to Git.
  * `package-lock.json` (will be created after first package install) - locks Package versions. Commit this to Git. 

**Install Packages (libraries)**

Look for packages at [npmjs](https://www.npmjs.com/). Contains package description, short documentation.

`npm install lodash` - install package.
`npm uninstall lodash` - uninstall package.


# Node

## Run JS file

Create file - e.g. `index.js`:
```
console.log('Hello World');
```
`node index.js` - run file, think of it as Main method in other languages.

## Example - use Package (library)

`index.js`:
```
// Load package to variable (use package name in require)
const _ = require('lodash');

// Use package
_.isString('text');
```

## Multiple Files

How to load other file:
* `require('./otherModule')` - file is `otherModule.js` in same folder.
* `require('./other/otherModule')` - file is in `other/otherModule.js` folder.
* `require('../otherModule')` - file is in parent folder from current file.


`index.js` - main file which will be run:
```
// Load other file to variable
const otherModule = require('./otherModule');

// Use it
otherModule.work();
```

`otherFile.js`:
```
// Private Code
function println(text) {
	console.log(text);
}

// module.exports - Public to other files
module.exports = {
	work() {
	    println('Working...');
	}
};
```

`node index.js` - run file.
