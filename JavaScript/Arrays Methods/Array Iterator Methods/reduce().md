# reduce()

- `reduce` is used to apply a function to each element in an array to reduce the array to a single value. It returns the final accumulated result.
- This method doesn't run the function if the array is empty, and it doesn't modify the original array.

## Usage

```jsx
let result = array.reduce(function(accumulator, currentValue, index, array) {
  // Your code here
  return updatedAccumulator;
}, initialValue);
```

## Example

**Example 1:** Summing all the elements of an array

```jsx
let numbers = [1, 2, 3, 4, 5];
let sum = numbers.reduce(function (accumulator, currentValue) {
  return accumulator + currentValue;
}, 0);
console.log(sum); // Output: 15
```

**Example 2:** Concatenating all elements of an array into a single string

```jsx
let words = ['Hello', ' ', 'world', '!'];
let sentence = words.reduce(function (accumulator, currentValue) {
  return accumulator + currentValue;
}, '');
console.log(sentence); // Output: 'Hello world!'
```