# Nested Functions

- Inner functions are functions defined within another function.
- They are also known as nested functions and have access to the outer (enclosing) function's variables and scope.

## Example

```jsx
function outerFunction() {
  let outerVar = 10;

  function innerFunction() {
    let innerVar = 5;
    return outerVar + innerVar;
  }

  return innerFunction();
}

let result = outerFunction();
console.log(result); // Output: 15
```

## Scopes

- Variables inside a function are only accessible within that function's scope.
- Functions can access variables and functions from their scope and any parent scopes.
- Functions defined in the global scope can access all global variables.
- Functions inside other functions can access variables from their parent function's scope and any other accessible variables.

```jsx
// The following let variables are defined in the global scope
let mid = 20;
let final = 5;
let fname = 'Ada';

// sum function is defined in the global scope
function sum() {
    return mid + final;
}
console.log(`#1 sum: ${sum()}`); // Returns 25

mid = 10;
console.log(`#2 sum: ${sum()}`); // Returns 15

function getScore() {
    let mid = 10;
    let final = 30;

    // yourScore is a nested function
    function yourScore() {
        return fname + ' scored ' + (mid + final);
    }

    return yourScore;
}

const score = getScore();
console.log(score()); // Returns "Ada scored 40"
```