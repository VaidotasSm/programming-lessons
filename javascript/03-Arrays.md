# Arrays
Arrays are just objects with properties: 0..N and with little bit magic added.

## Basics

```
let array1 = ['a', 'b', 'c'];
array1.length           // Size of array
array1[0];              // Get
array1[0] = 'cc';       // Change
array1.push('d');       // Add to the end
array1.pop();           //Remove - from end (and return)
array1.indexOf('a');    // position of element or "-1"
```

## Power Tools

**Sort**
```
array1.sort((a, b) => {return 0});  // return -1/0/1.
```

**For-each**
```
array1.forEach((e, index) => {});
```

**Filter elements that satisfy condition**
```
array1.filter((e, index) => e > 0);      // Find multiple (new array)
array1.find((e, index) => e > 0);        // Find one (first)
```

**Transform all elements**
```
array1.map((e, index) => e + 1);  // returns new array
```

**Reduce (sum) elements**
Useful when want to add/multiply/.. all elements.
```
let zeroSum = 0;
let sum = array.reduce((sum, e) => sum + e, zeroSum);
```
