# TypeScript

[Documentation](https://www.typescriptlang.org/)

TypeScript is a programming language that allows us to write JavaScript with a set of tools called a type system that can spot potential bugs in, clarify the structure of, and help refactor our code.

## How to use it

### 1.

We write TypeScript code in files with the extension `.ts`.

### 2.

We run our code through the TypeScript transpiler. The transpiler will check that the code adheres to TypeScript’s standards, and it will display errors when it does not.

TypeScript transpiler can be used on the command line by running the `tsc` command.

### 3.

If the TypeScript code can be converted into working JavaScript, the transpiler will output a JavaScript version of the file (.js).

## Type Inference

When we declare a variable with an initial value, the variable can never be reassigned a value of a different data type.

```
let order = 'first';

order = 1;
```

Error: `Type 'number' is not assignable to type 'string'.`

## Type Shapes

TypeScript knows what types our objects are, it also knows what shapes our objects adhere to. An object’s shape describes, among other things, what properties and methods it does or doesn’t contain.

```
"OH".length; // 2
"MY".toLowerCase(); // "my"
```

```
"MY".toLowercase();
// Property 'toLowercase' does not exist on type '"MY"'.
// Did you mean 'toLowerCase'?
```

## Type Any

Variables of type `any` can be assigned to any value and TypeScript won’t give an error if they’re reassigned to a different type later on.

```
let onOrOff;

onOrOff = 1;
onOrOff = false;
```

## Type Annotations

We can declare a variable and the type of the variable without an initial value.

We provide a type annotation by appending a variable with a colon `(:)` and the type (e.g., number, string, or any).

```
let mustBeAString : string;
mustBeAString = 'Catdog';

mustBeAString = 1337;
// Error: Type 'number' is not assignable to type 'string'
```