# Objects

## Object literal
```
let person = {
    name: 'John',
    surname: 'Smith',
    age: 30,
    printDescription() {
        console.log(`${this.name} ${this.surname} - ${this.age}`);
    }
};
person.age = 31;            // Get/Set property
person.country = 'USA';     // Add new property
delete person.country;      // Delete property
```










