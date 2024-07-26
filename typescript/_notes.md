# TypeScript

## Install TypeScript Globally

    npm install -g typescript

## Basic Type Annotation

Declare different variable types. Once declared as sepcific variable, TS will complain if you attempt to change it to another type. It will not stop it from compiling, but could cause issues.

```ts
// string declaration
let myVariable: string = "Some awesome string"

// number declaration
let numOfLives: number = 9
let numOfLives = "A string" // this will not work

// boolean declaration
let gameOver: boolean = false
```

TypeScript will infer types from certain variables based on the initial type.

```ts
// TS will infer this to be a string
let tvShow = "Lost"

// this will cause an error
tvShow = 8
```

The `any` type will allow you to change the type to whatever you want / need; TS will not complain in this case. The `any` type should be used sparingly. For example, it might be used if you are unsure what the type will be of a given variable.

```ts
// asign the any type
let thing: any = "hello"

// this causes no issues
thing = 400

// this will also be the any type
let var;
```

## Functions

Parameters will default to `any` if not explicitly typed.

```ts
// create function with explicit parameter type (number)
function square(num: number) {
	return num * num
}

// arrow function with multiple parameters (will need to be defined in order)
const doSomething = (person: string, age: number, isFunny: boolean) => {}

// default values can also be used in functions
function greet(person: string = "stranger") {
	"...do something"
}
```
