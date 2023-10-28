# every() and some()

# **`.every()`**

- Checks if all elements in an array pass a specified test, returning true if all elements meet the condition, and false if at least one does not.

## Usage

```jsx
let result = array.every(function(currentValue, index, array) {
  // Your code here
  return condition;
});
```

## Example

**Example 1:** Checking if all numbers are greater than 5

```jsx
let numbers = [6, 7, 8, 9, 10];
let allGreaterThanFive = numbers.every(function (number) {
  return number > 5;
});
console.log(allGreaterThanFive); // Output: true
```

**Example 2:** Checking if all words have more than 3 characters

```jsx
let words = ['apple', 'banana', 'cherry', 'date'];
let allMoreThanThree = words.every(function (word) {
  return word.length > 3;
});
console.log(allMoreThanThree); // Output: true
```