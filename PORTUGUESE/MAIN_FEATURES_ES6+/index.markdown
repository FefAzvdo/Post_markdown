# Principais features do ES6+ em JavaScript

## Let e Const

### Descrição

`let` e `const` são usados para declarar variáveis com escopo de bloco.

- **Quando usar**

  Use `let` para variáveis que podem mudar de valor e `const` para variáveis que não devem ser reatribuídas.

- **Como usar**

  ```javascript
  let x = 10;
  const y = 20;
  ```

- **Por que usar**

  Melhora a legibilidade e manutenção do código, além de evitar erros relacionados ao escopo.

### Exemplo

```javascript
let x = 10;
x = 20; // Válido

const y = 30;
y = 40; // Erro: Assignment to constant variable.
```

## Arrow Functions

### Descrição

Arrow functions são uma sintaxe mais curta para escrever funções.

- **Quando usar**

  Use arrow functions para funções curtas e quando você não precisa do próprio contexto `this`.

- **Como usar**

  ```javascript
  const add = (a, b) => a + b;
  ```

- **Por que usar**

  Sintaxe mais concisa e legibilidade melhorada.

### Exemplo

```javascript
const add = (a, b) => a + b;
console.log(add(2, 3)); // Output: 5
```

## Template Literals

### Descrição

Template literals permitem a interpolação de variáveis e expressões dentro de strings.

- **Quando usar**

  Use template literals para criar strings dinâmicas de forma mais legível.

- **Como usar**

  ```javascript
  const name = "John";
  const greeting = `Hello, ${name}!`;
  ```

- **Por que usar**

  Facilita a criação de strings complexas e melhora a legibilidade.

### Exemplo

```javascript
const name = "John";
const age = 30;
const greeting = `Hello, my name is ${name} and I am ${age} years old.`;
console.log(greeting); // Output: Hello, my name is John and I am 30 years old.
```

## Destructuring

### Descrição

Destructuring permite extrair valores de arrays ou propriedades de objetos em variáveis distintas.

- **Quando usar**

  Use destructuring para extrair valores de arrays ou objetos de forma mais concisa.

- **Como usar**

  ```javascript
  const [a, b] = [1, 2];
  const { name, age } = { name: "John", age: 30 };
  ```

- **Por que usar**

  Reduz a quantidade de código e melhora a clareza.

### Exemplo

```javascript
const [a, b] = [1, 2];
console.log(a); // Output: 1
console.log(b); // Output: 2

const { name, age } = { name: "John", age: 30 };
console.log(name); // Output: John
console.log(age); // Output: 30
```

## Spread Operator

### Descrição

O spread operator (`...`) permite expandir elementos de arrays ou objetos.

- **Quando usar**

  Use o spread operator para copiar arrays/objetos ou combinar múltiplos arrays/objetos.

- **Como usar**

  ```javascript
  const arr = [1, 2, 3];
  const newArr = [...arr, 4, 5];

  const obj = { a: 1, b: 2 };
  const newObj = { ...obj, c: 3 };
  ```

- **Por que usar**

  Facilita a manipulação de arrays e objetos de forma mais legível e concisa.

### Exemplo

```javascript
const arr = [1, 2, 3];
const newArr = [...arr, 4, 5];
console.log(newArr); // Output: [1, 2, 3, 4, 5]

const obj = { a: 1, b: 2 };
const newObj = { ...obj, c: 3 };
console.log(newObj); // Output: {a: 1, b: 2, c: 3}
```

## Promises

### Descrição

Promises são usadas para lidar com operações assíncronas.

- **Quando usar**

  Use promises para operações assíncronas como chamadas de API.

- **Como usar**

  ```javascript
  const promise = new Promise((resolve, reject) => {
    setTimeout(() => resolve("Success!"), 1000);
  });
  ```

- **Por que usar**

  Facilita o gerenciamento de operações assíncronas e melhora a legibilidade do código.

### Exemplo

```javascript
const promise = new Promise((resolve, reject) => {
  setTimeout(() => resolve("Success!"), 1000);
});

promise.then((result) => console.log(result)); // Output: Success!
```

## Async/Await

### Descrição

Async/await é uma sintaxe para trabalhar com promises de forma mais síncrona.

- **Quando usar**

  Use async/await para simplificar o código assíncrono baseado em promises.

- **Como usar**

  ```javascript
  async function fetchData() {
    const response = await fetch("https://api.example.com/data");
    const data = await response.json();
    return data;
  }
  ```

- **Por que usar**

  Melhora a legibilidade e facilita o tratamento de erros em operações assíncronas.

### Exemplo

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

### Descrição

Modules permitem a organização do código em arquivos separados e a reutilização de código.

- **Quando usar**

  Use modules para organizar e modularizar o código.

- **Como usar**

  ```javascript
  // module.js
  export const add = (a, b) => a + b;

  // main.js
  import { add } from "./module.js";
  console.log(add(2, 3)); // Output: 5
  ```

- **Por que usar**

  Facilita a manutenção e reutilização do código.

### Exemplo

```javascript
// module.js
export const add = (a, b) => a + b;

// main.js
import { add } from "./module.js";
console.log(add(2, 3)); // Output: 5
```

## Conclusão

Essas são algumas das principais funções do ES6+ em JavaScript.

Usar essas funcionalidades pode melhorar a legibilidade, manutenção e eficiência do seu código.
