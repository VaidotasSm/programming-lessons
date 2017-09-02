# Backend Development with Node and Express.js

Express.js - npm library for easier backend development.


## Working Example

1. Create folder.
2. `npm init` - create npm project.
3. `npm install express body-parser --save` - install packages you'll need. "Express" and "bodyParser" (for express to handle request body).
4. Create `index.js`:
```
const express = require('express');
const bodyParser = require('body-parser');

// Configure bodyParser
const app = express();
app.use(bodyParser.json());
app.use(bodyParser.urlencoded({ extended: true }));

// Middleware - before routes
app.use((req, res, next) => {
    console.log(`${req.originalUrl} - ${req.method}`);
    next();
});

// Routes
app.get('/hello', (req, res) => {
    res.status(200).json({ message: 'Hello!' });
});
app.get('*', (req, res) => {
    console.log(`404 - Not Found`);
    res.status(404).json({ message: 'Page not Found' });
});

const serverHandle = app.listen(8080, () => {
    console.log(`Started...`);
});
```
5. Modify `package.json`, under "scripts" there should be line starting with `"start": "node api/index.js"` - it is a script to start application:
```
"scripts": {
    "start": "node api/index.js"
},
```
6. Run from Terminal `npm run start` and go to http://localhost:8080/hello










