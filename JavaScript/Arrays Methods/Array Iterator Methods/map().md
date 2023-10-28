# map()

- Creates a new array by calling a function for every array element.
- Does not execute the function for empty elements.
- Does not change the original array.

## Usage

```jsx
let newArray = array.map(function(currentValue, index, array) {
  // Your code here
  return result; // must return
});
```

## Example

**Example 1:** Doubling each element of an array

```jsx
let numbers = [1, 2, 3, 4, 5];
let doubledNumbers = numbers.map(function (number) {
  return number * 2;
});
console.log(doubledNumbers); // Output: [2, 4, 6, 8, 10]
```

**Example 2:** Converting array of strings to uppercase

```jsx
let words = ["apple", "banana", "cherry"];
let uppercaseWords = words.map(function (word) {
  return word.toUpperCase();
});
console.log(uppercaseWords); // Output: ['APPLE', 'BANANA', 'CHERRY']
```