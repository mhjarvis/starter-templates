# TypeScript

## Install TypeScript Globally

    npm install -g typescript

## Basic Type Annotation

Declare different variable types. Once declared as sepcific variable, TS will complain if you attempt to change it to another type. It will not stop it from compiling, but could cause issues.

```ts
// DECLERATIONS
let myVariable: string = "Some awesome string" // string type
let numOfLives: number = 9 // number type
let numOfLives = "A string" // reasigning to different type will not work
let gameOver: boolean = false
```

TypeScript will infer types from certain variables based on the initial type.

```ts
// INFERENCE
let tvShow = "Lost" // infered to be a string
tvShow = 8 // this will cause an error
```

The `any` type will allow you to change the type to whatever you want / need; TS will not complain in this case. The `any` type should be used sparingly. For example, it might be used if you are unsure what the type will be of a given variable.

```ts
// THE ANY TYPE
let thing: any = "hello"
thing = 400  // reasignment to different type causes no issues
let var;  // this will also be of the any type
```

## Functions

Parameters will default to `any` if not explicitly typed. TypeScript is also smart enough to determine if a function will return multiple types.

```ts
// TYPE PARAMETERS IN FUNCTIONS
function square(num: number) {
	return num * num
}

// MULTIPLE PARAMETERS
const doSomething = (person: string, age: number, isFunny: boolean) => {}

// DEFAULT PARAMETERS
function greet(person: string = "stranger") {
	"...do something"
}

// RETURN TYPE
const addNums = (x: number, y: number): number => {
	return x + y
}

// VOID TYPE
function pr(): void {
	// this function does not return anything
	console.log("something")
}

// NEVER TYPE
function makeError(msg: string): never {
	// this function should never return anything
	throw new Error(msg)
}
```
