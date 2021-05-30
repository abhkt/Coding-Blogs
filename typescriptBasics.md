## What is Typescript?

- A JS superset
- A language building up on JS
- TS can't be executed by JS env like browsers/nodeJS
- it's a compiler which compiles your code in to JS
- [TS: A static type checker](https://www.typescriptlang.org/docs/handbook/typescript-from-scratch.html#typescript-a-static-type-checker)

## Core Types

The core primitive types in TypeScript are all lowercase!: [Types List](https://www.typescriptlang.org/docs/handbook/typescript-in-5-minutes.html#defining-types)

- [Primitive Types](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#the-primitives-string-number-and-boolean)
  - string
  - number
  - boolean
- [Array](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#arrays)
- [any](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#any)
- [function & contextual typing](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#functions)
- [object](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#object-types)
  - The type part of each property is also optional. If you don’t specify a type, it will be assumed to be any.
  - [optional properties](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#optional-properties)
    - when you read from an optional property, you’ll have to check for undefined before using it.
  - [union type](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#union-types)
    - TypeScript will only allow you to do things with the union if that thing is valid for every member of the union. For example, if you have the union string | number, you can’t use methods that are only available on string:
    - The solution is to narrow the union with code
    - If every member in a union has a property in common, you can use that property without narrowing:
  - [null & undefined](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#null-and-undefined)
    - we can use narrowing to check for values that might be null:
  - Enum

### [Type Aliases](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#type-aliases)

### [interface](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#interfaces)

- [type vs interface](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#differences-between-type-aliases-and-interfaces)
  - the key distinction is that a type cannot be re-opened to add new properties vs an interface which is always extendable.
  - interface with _extends_
  - type with _&_

### [Type Assertions](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#type-assertions)

### [Literal Types](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#literal-types)

TypeScript creates types for literals.

- set of specific values
- combining literals into unions
- can combine these with non-literal types:

---

A function is not allowed to return _undefined_ as its return type. we use void for that

### Tuples

### Enum

## [Type Inference](https://www.typescriptlang.org/docs/handbook/type-inference.html)

```ts
// type infered as number
let num1 = 5;

// type infered as number with a fix value 34
const num2 = 34;

// here it's important to define the type, default type is any
let num3;
```

Don't assign type of any var explicitly if TS can detect the type of that var. It's redundant
