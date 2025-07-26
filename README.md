# 14 Advanced JavaScript Concepts Before Your Next Interview

Based on @subhajit-adhikary’s guide to mastering advanced JavaScript concepts.

## Table of Contents

- [Callbacks](#callbacks)
- [Promises](#promises)
- [Async/Await](#asyncawait)
- [Strict Mode](#strict-mode)
- [Higher Order Functions](#higher-order-functions)
- [Call, Apply, Bind](#call-apply-bind)
- [Scope](#scope)
- [Closures](#closures)
- [Hoisting](#hoisting)
- [IIFE (Immediately Invoked Function Expressions)](#iife-immediately-invoked-function-expressions)
- [Currying](#currying)
- [Debouncing](#debouncing)
- [Throttling](#throttling)
- [Polyfills](#polyfills)

## Callbacks

A callback is a function passed into another function to be executed after its execution is complete. This pattern can result in callback hell when deeply nested.

## Promises

A Promise is an object representing the eventual completion or failure of an asynchronous operation.

```js
let fruits = ["apple", "banana", "kiwi"];

const animateOne = (fruit, animate) => {
  return new Promise((res, rej) => {
    setTimeout(() => {
      animate(fruit);
      res(true);
    }, 1000);
  });
};

const animateAll = (animate) => {
  animateOne(fruits[0], animate)
    .then(() => animateOne(fruits[1], animate))
    .then(() => animateOne(fruits[2], animate))
    .catch((err) => console.log("Some error occurred", err));
};

const animate = (fruit) => {
  console.log("animating", fruit);
};

animateAll(animate);
```

## Async/Await

Makes Promises more readable. Add `async` to declare; use `await` to pause for a Promise to resolve.

## Strict Mode

Use `"use strict";` to catch errors and write cleaner code.

```js
"use strict";
x = 56; // ReferenceError: x is not defined
```

## Higher Order Functions

Functions that take other functions as arguments or return a function.

## Call, Apply, Bind

- `.call()` changes `this` context & calls the function immediately.
- `.apply()` similar, but takes arguments as an array.
- `.bind()` returns a new function with a bound `this`.

```js
function fullName(greet) {
  console.log(greet + " " + this.firstName + " " + this.lastName);
}

const person1 = { firstName: "Elon", lastName: "Musk" };
fullName.call(person1, "Hello"); // Hello Elon Musk
```

## Scope

- **Block Scope**: `let`, `const`, only accessible inside `{ }`
- **Function Scope**: inside function
- **Global Scope**: outside any function/block

## Closures

A function combined with its lexical environment (outer variables/functions).

## Hoisting

Variable and function declarations are moved to the top of their scope before code execution. `var` and function declarations are hoisted.

## IIFE (Immediately Invoked Function Expressions)

A function that runs as soon as it is defined. Used for encapsulation/private scopes.

## Currying

Transforming a function with multiple arguments into a sequence of functions each with a single argument.

```js
function sum(a) {
  return function(b) {
    return function(c) {
      return a + b + c;
    }
  }
}
console.log(sum(3)(4)(5)); // 12
```

## Debouncing

Improves performance by delaying the function execution until after a certain period of inactivity.

## Throttling

Limits a function to run only once within a specified time interval.

```js
function throttle(fx, delay) {
  let timeoutId = null;
  return function() {
    if (!timeoutId) {
      timeoutId = setTimeout(() => {
        fx();
        clearTimeout(timeoutId);
        timeoutId = null;
      }, delay);
    }
  }
}
```

## Polyfills

Code that implements features not supported by a browser, often by modifying native prototypes.
