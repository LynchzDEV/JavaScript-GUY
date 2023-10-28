# Pass Function to Other Functions

**For example:** `filter` function in JavaScript is used to create a new array containing only the elements that pass a specific test. It takes in a function as an argument, which can be an arrow function or a callback function.

**1. Arrow function passing to filter function**

```jsx
const words = [
  "spray",
  "limit",
  "elite",
  "exuberant",
  "destruction",
  "present",
];
const result = words.filter((word) => word.length > 6);
console.log(result);
// expected output: Array ["exuberant", "destruction", "present"]
```

**2. Callback function passing to filter function**

```jsx
function isMorethanFive(value) {
  return value > 5;
}
const filterNums = [12, 5, 8, 130, 44].filter(isMorethanFive);
// filterNums is [12, 8, 130, 44]
```

**3. Inline callback function passing to filter function**

```jsx
const nums = [-3, -2, -1, 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13];
const primeNums = nums.filter(function (num) {
  for (let i = 2; num > i; i++) {
    if (num % i === 0) {
      return false;
    }
  }
  return num > 1;
});
// primeNums is [ 2, 3, 5, 7, 11, 13 ]
```