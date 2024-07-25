# TypeScript

## Install TypeScript Globally

    npm install -g typescript

### Basic Type Annotation

Declare different variable types. Once declared as sepcific variable, TS will complain if you attempt to change it to another type.

```ts
// string declaration
let myVariable: string = "Some awesome string"

// number declaration
let numOfLives: number = 9
let numOfLives = "A string" // this will not work

// boolean declaration
let gameOver: boolean = false
```
