# concat()

- Merge two or more arrays, creating a new array without changing the existing arrays.

## Usage

```jsx
let newArray = array1.concat(array2, array3, ..., arrayN);
```

## Example

**Example 1:** Concatenating two arrays

```jsx
let array1 = [1, 2, 3];
let array2 = [4, 5, 6];
let mergedArray = array1.concat(array2);
console.log(mergedArray); // Output: [1, 2, 3, 4, 5, 6]
```

**Example 2:** Concatenating multiple arrays

```jsx
let array3 = ['a', 'b', 'c'];
let array4 = ['d', 'e', 'f'];
let array5 = ['g', 'h', 'i'];
let multipleArrays = array3.concat(array4, array5);
console.log(multipleArrays); // Output: ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i']
```