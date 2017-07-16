# Control Structures

**Variable Declaration**
```
let name1 = 'John';     // Recommended - variable
const name2 = 'John';   // Recommended - constant
var name3 = 'John';     // Not Recommended - function scope variable
```

**Conditionals**
Use `===` (`!==`) instead of `==` (`!=`). When using `==` JavaScript tries to help by converting values so you can get unexpected results e.g. `true == 1` is true, while `true === 1` is false.

```
if (name === 'A'){ }
else if(name === 'B') { }
else { }
```

```
let text = name === 'A' ? 'AAA' : 'Other';
```

Conditional Operators:
`x && y` - AND.
`x || y` - OR.


**Loops**
```
for (let i = 0; i <= 10; i = i + 1){
    console.log(i);
}
```

```
let i = 0;
while (i < 10) {
    console.log(i);
    i = i + 1;
}
```

# Data Types

# null and undefined
```
let x;              // Undefined
let x = undefined;  // Undefined
let y = null;       // null
```


## Boolean
```
let t = true;
let f = false;
```


## Number
```
let count = 10;
let sum = count + 5;
```

**Math object**
```
Math.round(5.5)         // 6  
Math.ceil(5.1);         // 6
Math.floor(5.9);        // 5
Math.max(1, 2, 3, 4);   // 4 - finds max
Math.min(1, 2, 3, 4);   // 1 - find min
```
Math contains lots more useful functions...


## String
```
let text1 = 'Some text';    // Recommended
let text2 = "Some text";
```

**With Variables**
```
let name = 'John'
let text3 = 'Hello ${name}'
```

**Useful**

text.length; - how many symbols?
text.indexOf('word'); - get starting position of search text. Returns `-1` if not found.

## Date

```
let date = new Date();
new Date(2000, 0, 1);
new Date(2000, 0, 1, 1, 1, 1);
```