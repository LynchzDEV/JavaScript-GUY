# filter()

- Creates a new array with all elements that pass the test implemented by the provided function.

## Usage

```jsx
let newArray = array.filter(function(currentValue, index, array) {
  // Your code here
  return condition; // must return
});
```

## Example

**Example 1:** Filtering even numbers from an array

```jsx
let numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let evenNumbers = numbers.filter(function (number) {
  return number % 2 === 0;
});
console.log(evenNumbers); // Output: [2, 4, 6, 8, 10]
```

**Example 2:** Filtering words with more than 5 characters

```jsx
let words = ['apple', 'banana', 'cherry', 'date', 'elderberry'];
let longWords = words.filter(function (word) {
  return word.length > 5;
});
console.log(longWords); // Output: ['banana', 'cherry', 'elderberry']
```