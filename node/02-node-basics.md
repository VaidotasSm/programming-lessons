# Node

## Run JS file

Create file - e.g. `index.js`:
```
console.log('Hello World');
```
`node index.js` - run file (Terminal), think of it as Main method in other languages.

## Multiple Files

How to load other file:
* `require('./otherModule')` - file is `otherModule.js` in same folder.
* `require('./other/otherModule')` - file is in `other/otherModule.js` folder.
* `require('../otherModule')` - file is in parent folder from current file.

**Example**

`index.js` - main file which will be run:
```
// Load other file to variable
const otherModule = require('./otherModule');

// Use it
otherModule.work();
```

`otherFile.js` - other file:
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
