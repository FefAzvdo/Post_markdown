# Introduction to TypeScript

## What is TypeScript?

TypeScript is a superset of JavaScript developed by Microsoft that adds optional static typing and other advanced features to JavaScript. It allows developers to write safer and more maintainable code by catching errors at compile time instead of runtime.

## How to Implement TypeScript in a JavaScript Project

1. **Install TypeScript**:
   To start using TypeScript, you need to install it globally on your system. Use the following command in the terminal:

   ```sh
   npm install -g typescript
   ```

2. **Initialize a TypeScript Project**:
   Create a `tsconfig.json` file in the root directory of your project. This file configures the TypeScript compiler options.

   ```sh
   tsc --init
   ```

3. **Write TypeScript Code**:
   Rename your JavaScript files (`.js`) to TypeScript files (`.ts`) and start adding static typing and other TypeScript features.

4. **Compile TypeScript Code**:
   Use the `tsc` command to compile your TypeScript files into JavaScript.
   ```sh
   tsc
   ```

## Main Features of TypeScript

### Static Typing

TypeScript allows you to define types for variables, function parameters, and function returns, helping to avoid common errors.

```typescript
let name: string = "Fernando";
let age: number = 30;

function greet(name: string): string {
  return `Hello, ${name}`;
}
```

### Interfaces

Interfaces define contracts for objects, ensuring they have certain properties and methods.

```typescript
interface Person {
  name: string;
  age: number;
}

const person: Person = {
  name: "Fernando",
  age: 30,
};
```

### Classes and Inheritance

TypeScript supports classes and inheritance, allowing the creation of object-oriented code structures.

```typescript
class Animal {
  name: string;

  constructor(name: string) {
    this.name = name;
  }

  move(distance: number): void {
    console.log(`${this.name} moved ${distance} meters.`);
  }
}

class Dog extends Animal {
  bark(): void {
    console.log("Woof woof!");
  }
}

const dog = new Dog("Rex");
dog.bark();
dog.move(10);
```

### Enumerations (Enums)

Enums allow you to define a set of named values.

```typescript
enum Color {
  Red,
  Green,
  Blue,
}

let favoriteColor: Color = Color.Green;
```

### Generic Types

Generics allow you to create reusable components that work with various types.

```typescript
function identity<T>(value: T): T {
  return value;
}

let number = identity<number>(10);
let text = identity<string>("Hello");
```

### Union and Intersection Types

Union types allow a variable to have more than one type.

```typescript
let id: number | string;
id = 10;
id = "ten";
```

Intersection types combine multiple types into one.

```typescript
interface A {
  a: string;
}

interface B {
  b: string;
}

type AB = A & B;

const ab: AB = { a: "A", b: "B" };
```

## Conclusion

TypeScript is a powerful tool that improves the quality of JavaScript code by providing static typing and other advanced features. Adopting TypeScript can help avoid many common errors and make software development more efficient and secure.
