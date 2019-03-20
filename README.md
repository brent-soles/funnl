# Welcome to a super punny package

### fun.js ###

The main purpose of this package is to have a group of functions that have a functional aspect to them.

### WARNING ###

This package is currently under development.

### To start ###

Clone the repo, then run `npm install` or `yarn init`

### Code examples ###

```javascript

// Import
const { pipe } = require('funjs');

// Two ways:

// First is to use callback functions
const res = pipe([
  () => "Hello",
  (hello) => `${hello} World!` 
]);
console.log(res); // "Hello Wprld!"
...

// Second, define, and then pass functions
// Notice, when a function has more than one argument,
// we pass an array with the first element being the function.
// The result of the first element in the pipe is then passed
// as the first arg of the next function call, then
// the rest of the args get passed along, so the eventual
// function call looks like:
//   add(2, 8)
// given the example below.
const add(a, b) => a + b;
const res = pipe([
  2,
  [add, 8]
]);
console.log(res) // 10
```