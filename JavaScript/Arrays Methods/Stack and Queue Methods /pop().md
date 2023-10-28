# pop()

- **Removes the last element** from an array and returns that element. This operation modifies the original array.

## Usage

```jsx
let removedElement = array.pop();
```

## Example

**Example 1:** Removing the last element from an array

```jsx
let fruits = ['apple', 'banana', 'cherry'];
let removedFruit = fruits.pop();
console.log(removedFruit); // Output: 'cherry'
console.log(fruits); // Output: ['apple', 'banana']
```

**Example 2:** Removing and using the last element of an array

```jsx
let numbers = [1, 2, 3, 4, 5];
let lastNumber = numbers.pop();
console.log(lastNumber); // Output: 5
console.log(numbers); // Output: [1, 2, 3, 4]
```