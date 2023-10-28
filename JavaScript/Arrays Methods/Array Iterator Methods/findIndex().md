# findIndex()

- Returns the index of the first element in an array that satisfies the provided testing function. If no element passes the test, it returns -1.

## Usage

```jsx
let resultIndex = array.findIndex(function(currentValue, index, array) {
  // Your code here
  return condition; // must return
});
```

## Example

**Example 1:** Finding the index of the first element greater than 4

```jsx
let numbers = [1, 3, 5, 7, 9, 2, 4, 6, 8];
let foundIndex = numbers.findIndex(function (number) {
  return number > 4;
});
console.log(foundIndex); // Output: 2
```

**Example 2:** Finding the index of a specific string in an array

```jsx
let words = ['apple', 'banana', 'cherry', 'date'];
let foundIndexWord = words.findIndex(function (word) {
  return word === 'cherry';
});
console.log(foundIndexWord); // Output: 2
```