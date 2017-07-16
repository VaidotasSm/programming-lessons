# Testing Basics

## Mocha Test Runner
Runs .js test files.

**Install**
Instal "mocha" test runner to run your tests:
* `npm install mocha --save-dev` (recommended) - save locally and use in package.json scripts.
* `npm install mocha -g` - install globally. 

**Commands (global or in "scripts")**
* `mocha` - run tests in `/test` folder.
* `mocha --recursive` - run tests in `/test` folder and include sub-folders.
* `mocha testing/**/*.js` - specify folder (includes all .js files and sub-folders).

**Test file structure**
```
const assert = require('assert');

before(() => console.log('Before all tests started'));
after(() => console.log('After all tests finished'));

describe('Test Suite 1', function() {
    before(() => console.log('Before all tests in this Suite'));
    after(() => console.log('After all tests in this Suite'));

    it('test 1', () => {});
    it('test 2', () => {});
});

describe('Test Suite 2', function() {
    before(() => console.log('Before all tests in this Suite'));
    after(() => console.log('Before all tests in this Suite'));

    it('test 3', () => {});
    it('test 4', () => {});
});
```

## Assert - Node assertions
Assertions is library to compare values in your tests. Node has this library built-in, don't need to install.

**Example**
```
const assert = require('assert');

let actual = ...;
let expected = ...;
assert.equal(actual, expected);     // is Equal?
assert.notEqual(actual, expected);  // is Not Equal?
assert.ok(actual);                  // is True-thy
```

Truthy - value that is treated in JavaScript like boolean `true` - true, > 0, not null/undefined, not empty string...


## Full Example

* `calc/index.js` - code to be tested.
```
module.exports = {
    add(a, b) {
        return a + b;
    },
    subtract(a, b) {
        return a - b;
    }
};
```

* `test/calc.test.js`
```
const assert = require('assert');
const calc = require('../calc/index');

before(() => console.log('Before all tests'));
after(() => console.log('After all tests'));

describe('Addition functionality', function() {
    before(() => console.log('Before all tests 1'));
    after(() => console.log('After all tests 1'));

    it('should add valid numbers', () => {
        assert.equal(calc.add(1, 2), 3);
    });
});

describe('Subtraction functionality', function() {
    before(() => console.log('Before all tests 2'));
    after(() => console.log('After all tests 2'));

    it('should subtract smaller number', () => {
        assert.equal(calc.subtract(5, 2), 3);
    });
});
```

* `package.json` - declare script:
```
"scripts": {
    "test": "mocha --recursive"
},
```

* `npm run test` - run your tests.





