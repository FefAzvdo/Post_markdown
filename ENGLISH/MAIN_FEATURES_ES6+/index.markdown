# Main features of ES6+ in JavaScript

## Let and Const

### Description

`let` and `const` are used to declare variables with block scope.

- **When to use**

Use `let` for variables that can change value and `const` for variables that should not be reassigned.

- **How ​​to use**

```javascript
let x = 10;
const y = 20;
```

- **Why to use**

Improves readability and maintainability of code, in addition to avoiding scope-related errors.

### Example

```javascript
let x = 10;
x = 20; // Valid

const y = 30;
y = 40; // Error: Assignment to constant variable.
```

## Arrow Functions

### Description

Arrow functions are a shorter syntax for writing functions.

- **When to use**

Use arrow functions for short functions and when you don't need the `this` context itself.

- **How ​​to use**

```javascript
const add = (a, b) => a + b;
```

- **Why to use**

More concise syntax and improved readability.

### Example

```javascript
const add = (a, b) => a + b;
console.log(add(2, 3)); // Output: 5
```

## Template Literals

### Description

Template literals allow you to interpolate variables and expressions within strings.

- **When to use**

Use template literals to create dynamic strings in a more readable way.

- **How ​​to use**

```javascript
const name = "John";
const greeting = `Hello, ${name}!`;
```

- **Why to use**

Makes it easier to create complex strings and improves readability.

### Example

```javascript
const name = "John";
const age = 30;
const greeting = `Hello, my name is ${name} and I am ${age} years old.`;
console.log(greeting); // Output: Hello, my name is John and I am 30 years old.
```

## Destructuring

### Description

Destructuring allows you to extract values ​​from arrays or properties of objects into separate variables.

- **When to use**

Use destructuring to extract values ​​from arrays or objects in a more concise way.

- **How ​​to use**

```javascript
const [a, b] = [1, 2];
const { name, age } = { name: "John", age: 30 };
```

- **Why to use**

Reduces the amount of code and improves clarity.

### Example

```javascript
const [a, b] = [1, 2];
console.log(a); // Output: 1
console.log(b); // Output: 2

const { name, age } = { name: "John", age: 30 };
console.log(name); // Output: John
console.log(age); // Output: 30
```

## Spread Operator

### Description

The spread operator (`...`) allows you to expand elements of arrays or objects.

- **When to use**

Use the spread operator to copy arrays/objects or combine multiple arrays/objects.

- **How ​​to use**

```javascript
const arr = [1, 2, 3];
const newArr = [...arr, 4, 5];
const obj = { a: 1, b: 2 };
const newObj = { ...obj, c: 3 };
```

- **Why use**

It makes manipulating arrays and objects easier and more concise.

### Example

```javascript
const arr = [1, 2, 3];
const newArr = [...arr, 4, 5];
console.log(newArr); // Output: [1, 2, 3, 4, 5]

const obj = { a: 1, b: 2 };
const newObj = { ...obj, c: 3 };
console.log(newObj); // Output: {a: 1, b: 2, c: 3}
```

## Promises

### Description

Promises are used to handle asynchronous operations.

- **When to use**

Use promises for asynchronous operations like API calls.

- **How ​​to use**

````javascript
const promise = new Promise((resolve, reject) => {
setTimeout(() => resolve("Success!"), 1000);
}); ```

- **Why use it**

It makes it easier to manage asynchronous operations and improves code readability.

### Example

```javascript
const promise = new Promise((resolve, reject) => {
setTimeout(() => resolve("Success!"), 1000);
});

promise.then((result) => console.log(result)); // Output: Success!
````

## Async/Await

### Description

Async/await is a syntax for working with promises in a more synchronous way.

- **When to use it**

Use async/await to simplify asynchronous code based on promises.

- **How ​​to use it**

```javascript
async function fetchData() {
  const response = await fetch("https://api.example.com/data");
  const data = await response.json();
  return data;
}
```

- **Why use it**

Improves readability and makes it easier to handle errors in asynchronous operations.

### Example

```javascript
async function fetchData() {
  try {
    const response = await fetch("https://api.example.com/data");
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error("Error fetching data:", error);
  }
}
fetchData();
```

## Modules

### Description

Modules allow you to organize your code into separate files and reuse code.

- **When to use it**

Use modules to organize and modularize your code.

- **How ​​to use**

```javascript
// module.js
export const add = (a, b) => a + b;

// main.js
import { add } from "./module.js";
console.log(add(2, 3)); // Output: 5
```

- **Why use**

It makes code easier to maintain and reuse.

### Example

```javascript
// module.js
export const add = (a, b) => a + b;

// main.js
import { add } from "./module.js";
console.log(add(2, 3)); // Output: 5
```

## Conclusion

These are some of the main ES6+ functions in JavaScript.

Using these features can improve the readability, maintainability, and efficiency of your code.
