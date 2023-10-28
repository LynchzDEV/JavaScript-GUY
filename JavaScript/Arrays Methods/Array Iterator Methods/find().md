# find()

- Returns the value of the first element in an array that satisfies the provided testing function.

## Usage

```jsx
let result = array.find(function(currentValue, index, array) {
  // Your code here
  return condition; // must return
});
```

## Example

**Example 1:** Finding the first element that is greater than 4

```jsx
let numbers = [1, 3, 5, 7, 9, 2, 4, 6, 8];
let foundNumber = numbers.find(function (number) {
  return number > 4;
});
console.log(foundNumber); // Output: 5
```

**Example 2:** Finding a specific string in an array

```jsx
let words = ['apple', 'banana', 'cherry', 'date'];
let foundWord = words.find(function (word) {
  return word === 'cherry';
});
console.log(foundWord); // Output: 'cherry'
```