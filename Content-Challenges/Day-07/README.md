# Table Of Content

- [Table Of Content](#table-of-content)
- [Day 7: Arrays and Objects](#day-7-arrays-and-objects)
  - [Tasks/Activities](#tasksactivities)
    - [Activity 1: Array Manipulation](#activity-1-array-manipulation)
      - [Task 1: Write a function to add an element to the end of an array and return the new array.](#task-1-write-a-function-to-add-an-element-to-the-end-of-an-array-and-return-the-new-array)
      - [Task 2: Write a function to remove the first element from an array and return the new array.](#task-2-write-a-function-to-remove-the-first-element-from-an-array-and-return-the-new-array)
    - [Activity 2: Array Iteration](#activity-2-array-iteration)
      - [Task 3: Write a function to iterate over an array and log each element to the console.](#task-3-write-a-function-to-iterate-over-an-array-and-log-each-element-to-the-console)
      - [Task 4: Write a function to create a new array with the squares of each element from the original array.](#task-4-write-a-function-to-create-a-new-array-with-the-squares-of-each-element-from-the-original-array)
    - [Activity 3: Object Manipulation](#activity-3-object-manipulation)
      - [Task 5: Write a function to add a new property to an object and return the updated object.](#task-5-write-a-function-to-add-a-new-property-to-an-object-and-return-the-updated-object)
      - [Task 6: Write a function to remove a property from an object and return the updated object.](#task-6-write-a-function-to-remove-a-property-from-an-object-and-return-the-updated-object)
    - [Activity 4: Object Iteration](#activity-4-object-iteration)
      - [Task 7: Write a function to iterate over an object's properties and log each key-value pair to the console.](#task-7-write-a-function-to-iterate-over-an-objects-properties-and-log-each-key-value-pair-to-the-console)
      - [Task 8: Write a function to create a new object with the squares of each value from the original object.](#task-8-write-a-function-to-create-a-new-object-with-the-squares-of-each-value-from-the-original-object)
    - [Activity 5: Combining Arrays and Objects](#activity-5-combining-arrays-and-objects)
      - [Task 9: Write a function to create an array of objects from two arrays, one with keys and one with values.](#task-9-write-a-function-to-create-an-array-of-objects-from-two-arrays-one-with-keys-and-one-with-values)
      - [Task 10: Write a function to merge two arrays of objects based on a common key.](#task-10-write-a-function-to-merge-two-arrays-of-objects-based-on-a-common-key)
  - [Achievement](#achievement)

# Day 7: Arrays and Objects

## Tasks/Activities

### Activity 1: Array Manipulation

#### Task 1: Write a function to add an element to the end of an array and return the new array.

```javascript
function addElementToEnd(arr, element) {
  arr.push(element);
  return arr;
}

// Example usage:
console.log(addElementToEnd([1, 2, 3], 4)); // Output: [1, 2, 3, 4]
```

**Explanation:** This function takes an array and an element as input, adds the element to the end of the array using the `push` method, and returns the modified array.

#### Task 2: Write a function to remove the first element from an array and return the new array.

```javascript
function removeFirstElement(arr) {
  arr.shift();
  return arr;
}

// Example usage:
console.log(removeFirstElement([1, 2, 3])); // Output: [2, 3]
```

**Explanation:** This function takes an array as input, removes the first element using the `shift` method, and returns the modified array.

### Activity 2: Array Iteration

#### Task 3: Write a function to iterate over an array and log each element to the console.

```javascript
function logArrayElements(arr) {
  arr.forEach(element => console.log(element));
}

// Example usage:
logArrayElements([1, 2, 3]);
// Output:
// 1
// 2
// 3
```

**Explanation:** This function takes an array as input and uses the `forEach` method to iterate over each element, logging it to the console.

#### Task 4: Write a function to create a new array with the squares of each element from the original array.

```javascript
function squareArrayElements(arr) {
  return arr.map(element => element * element);
}

// Example usage:
console.log(squareArrayElements([1, 2, 3])); // Output: [1, 4, 9]
```

**Explanation:** This function takes an array as input and uses the `map` method to create a new array with the squares of each element from the original array.

### Activity 3: Object Manipulation

#### Task 5: Write a function to add a new property to an object and return the updated object.

```javascript
function addObjectProperty(obj, key, value) {
  obj[key] = value;
  return obj;
}

// Example usage:
console.log(addObjectProperty({a: 1, b: 2}, 'c', 3)); // Output: {a: 1, b: 2, c: 3}
```

**Explanation:** This function takes an object, a key, and a value as input, adds the new property to the object, and returns the updated object.

#### Task 6: Write a function to remove a property from an object and return the updated object.

```javascript
function removeObjectProperty(obj, key) {
  delete obj[key];
  return obj;
}

// Example usage:
console.log(removeObjectProperty({a: 1, b: 2, c: 3}, 'b')); // Output: {a: 1, c: 3}
```

**Explanation:** This function takes an object and a key as input, removes the property with the specified key from the object using the `delete` operator, and returns the updated object.

### Activity 4: Object Iteration

#### Task 7: Write a function to iterate over an object's properties and log each key-value pair to the console.

```javascript
function logObjectProperties(obj) {
  for (let key in obj) {
    if (obj.hasOwnProperty(key)) {
      console.log(`${key}: ${obj[key]}`);
    }
  }
}

// Example usage:
logObjectProperties({a: 1, b: 2, c: 3});
// Output:
// a: 1
// b: 2
// c: 3
```

**Explanation:** This function takes an object as input and uses a `for...in` loop to iterate over its properties, logging each key-value pair to the console. The `hasOwnProperty` method ensures that only the object's own properties are logged, not inherited properties.

#### Task 8: Write a function to create a new object with the squares of each value from the original object.

```javascript
function squareObjectValues(obj) {
  let newObj = {};
  for (let key in obj) {
    if (obj.hasOwnProperty(key)) {
      newObj[key] = obj[key] * obj[key];
    }
  }
  return newObj;
}

// Example usage:
console.log(squareObjectValues({a: 1, b: 2, c: 3})); // Output: {a: 1, b: 4, c: 9}
```

**Explanation:** This function takes an object as input and creates a new object with the squares of each value from the original object. It uses a `for...in` loop to iterate over the properties and the `hasOwnProperty` method to ensure only the object's own properties are processed.

### Activity 5: Combining Arrays and Objects

#### Task 9: Write a function to create an array of objects from two arrays, one with keys and one with values.

```javascript
function createObjectArray(keys, values) {
  let result = [];
  for (let i = 0; i < keys.length; i++) {
    let obj = {};
    obj[keys[i]] = values[i];
    result.push(obj);
  }
  return result;
}

// Example usage:
console.log(createObjectArray(['a', 'b', 'c'], [1, 2, 3])); // Output: [{a: 1}, {b: 2}, {c: 3}]
```

**Explanation:** This function takes two arrays, one with keys and one with values, and creates an array of objects where each object has a single key-value pair from the corresponding elements of the input arrays.

#### Task 10: Write a function to merge two arrays of objects based on a common key.

```javascript
function mergeObjectArrays(arr1, arr2, key) {
  let mergedArray = [];
  arr1.forEach(obj1 => {
    let obj2 = arr2.find(obj => obj[key] === obj1[key]);
    if (obj2) {
      mergedArray.push({...obj1, ...obj2});
    }
  });
  return mergedArray;
}

// Example usage:
const array1 = [{id: 1, name: 'Alice'}, {id: 2, name: 'Bob'}];
const array2 = [{id: 1, age: 25}, {id: 2, age: 30}];
console.log(mergeObjectArrays(array1, array2, 'id'));
// Output: [{id: 1, name: 'Alice', age: 25}, {id: 2, name: 'Bob', age: 30}]
```

**Explanation:** This function takes two arrays of objects and a common key, and merges the objects from both arrays based on the common key. It uses the `find` method to locate the matching object in the second array and the spread operator to merge the objects.

## Achievement

By the end of these activities, students will:

- Understand and manipulate arrays using various methods.
- Iterate over arrays and objects to perform operations on their elements and properties.
- Create and modify objects dynamically.
- Combine arrays and objects to solve complex data manipulation tasks.
- Enhance their ability to work with data structures in JavaScript.
