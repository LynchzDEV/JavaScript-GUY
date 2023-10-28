# JSON: JavaScript Object Notation

Go read this, I’m lazy.

[Javascript Object Notation (JSON)](https://medium.com/@pakawatmange/javascript-object-notation-json-886824916823)

## `JSON.stringify`

converts a value to the ***JSON*** notation

```jsx
const person = {
  name: 'Blue',
};
console.log(JSON.stringify(person)); // { "name": "Blue" }
```

## Example of benefits from `JSON.stringify`

- **Check if the object is empty**
    
    ```jsx
    const myObj = {};
    if (JSON.stringify(myObj) === '{}') {
      console.log('The object is empty!');
    }
    ```
    
    ![The result of the above code](JSON%20JavaScript%20Object%20Notation%205c351381793d44c58b3f36cc59c0da3e/Screenshot_2023-10-15_at_18.47.37.png)
    
    The result of the above code
    
    Alternate way without using `JSON.stringify`
    
    ```jsx
    const myObj = {};
    if (Object.keys(myObj).length === 0) {
      console.log('The object is empty!');
    }
    ```