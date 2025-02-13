# Introdução ao TypeScript

## O que é TypeScript?

TypeScript é um superconjunto de JavaScript desenvolvido pela Microsoft que adiciona tipagem estática opcional e outros recursos avançados ao JavaScript. Ele permite que os desenvolvedores escrevam código mais seguro e mantenível, detectando erros em tempo de compilação em vez de tempo de execução.

## Como implementar TypeScript em um projeto JavaScript

1. **Instalar o TypeScript**:
   Para começar a usar TypeScript, você precisa instalá-lo globalmente no seu sistema. Use o seguinte comando no terminal:

   ```sh
   npm install -g typescript
   ```

2. **Inicializar um projeto TypeScript**:
   Crie um arquivo `tsconfig.json` no diretório raiz do seu projeto. Este arquivo configura as opções do compilador TypeScript.

   ```sh
   tsc --init

   ```

3. **Escrever código TypeScript**:
   Renomeie seus arquivos JavaScript (`.js`) para arquivos TypeScript (`.ts`) e comece a adicionar tipagem estática e outros recursos do TypeScript.

4. **Compilar o código TypeScript**:
   Use o comando `tsc` para compilar seus arquivos TypeScript em JavaScript.
   ```sh
   tsc
   ```

## Principais Features do TypeScript

### Tipagem Estática

TypeScript permite definir tipos para variáveis, parâmetros de função e retornos de função, ajudando a evitar erros comuns.

```typescript
let nome: string = "Fernando";
let idade: number = 30;

function saudar(nome: string): string {
  return `Olá, ${nome}`;
}
```

### Interfaces

Interfaces definem contratos para objetos, garantindo que eles tenham certas propriedades e métodos.

```typescript
interface Pessoa {
  nome: string;
  idade: number;
}

const pessoa: Pessoa = {
  nome: "Fernando",
  idade: 30,
};
```

### Classes e Herança

TypeScript suporta classes e herança, permitindo a criação de estruturas de código orientadas a objetos.

```typescript
class Animal {
  nome: string;

  constructor(nome: string) {
    this.nome = nome;
  }

  mover(distancia: number): void {
    console.log(`${this.nome} moveu ${distancia} metros.`);
  }
}

class Cachorro extends Animal {
  latir(): void {
    console.log("Au au!");
  }
}

const cachorro = new Cachorro("Rex");
cachorro.latir();
cachorro.mover(10);
```

### Enumerações (Enums)

Enums permitem definir um conjunto de valores nomeados.

```typescript
enum Cor {
  Vermelho,
  Verde,
  Azul,
}

let corFavorita: Cor = Cor.Verde;
```

### Tipos Genéricos

Generics permitem criar componentes reutilizáveis que funcionam com vários tipos.

```typescript
function identidade<T>(valor: T): T {
  return valor;
}

let numero = identidade<number>(10);
let texto = identidade<string>("Olá");
```

### Tipos de União e Interseção

Union types permitem que uma variável tenha mais de um tipo.

```typescript
let id: number | string;
id = 10;
id = "dez";
```

Intersection types combinam múltiplos tipos em um.

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

## Conclusão

TypeScript é uma poderosa ferramenta que melhora a qualidade do código JavaScript, fornecendo tipagem estática e outros recursos avançados. Adotar TypeScript pode ajudar a evitar muitos erros comuns e tornar o desenvolvimento de software mais eficiente e seguro.
