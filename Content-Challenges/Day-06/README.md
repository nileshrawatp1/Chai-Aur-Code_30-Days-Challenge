# Table Of Content

- [Table Of Content](#table-of-content)
- [Day 6: Arrays and Objects](#day-6-arrays-and-objects)
  - [Tasks/Activities](#tasksactivities)
    - [Activity 1: Arrays](#activity-1-arrays)
      - [Task 1: Create an array of numbers and log the array to the console.](#task-1-create-an-array-of-numbers-and-log-the-array-to-the-console)
      - [Task 2: Write a function to find the sum of all elements in an array and return the result.](#task-2-write-a-function-to-find-the-sum-of-all-elements-in-an-array-and-return-the-result)
      - [Task 3: Write a function to find the maximum element in an array and return the result.](#task-3-write-a-function-to-find-the-maximum-element-in-an-array-and-return-the-result)
    - [Activity 2: Objects](#activity-2-objects)
      - [Task 4: Create an object representing a person with properties for name, age, and city. Log the object to the console.](#task-4-create-an-object-representing-a-person-with-properties-for-name-age-and-city-log-the-object-to-the-console)
      - [Task 5: Write a function to log a greeting message using the properties of the person object.](#task-5-write-a-function-to-log-a-greeting-message-using-the-properties-of-the-person-object)
    - [Activity 3: Array of Objects](#activity-3-array-of-objects)
      - [Task 6: Create an array of objects representing different people, each with properties for name, age, and city. Log the array to the console.](#task-6-create-an-array-of-objects-representing-different-people-each-with-properties-for-name-age-and-city-log-the-array-to-the-console)
      - [Task 7: Write a function to find the person with the maximum age in the array and return the person's object.](#task-7-write-a-function-to-find-the-person-with-the-maximum-age-in-the-array-and-return-the-persons-object)
    - [Activity 4: Array Methods](#activity-4-array-methods)
      - [Task 8: Write a function to filter the array of people to only include those who live in a specific city and return the filtered array.](#task-8-write-a-function-to-filter-the-array-of-people-to-only-include-those-who-live-in-a-specific-city-and-return-the-filtered-array)
      - [Task 9: Write a function to sort the array of people by age in ascending order and return the sorted array.](#task-9-write-a-function-to-sort-the-array-of-people-by-age-in-ascending-order-and-return-the-sorted-array)
    - [Activity 5: Combining Arrays and Objects](#activity-5-combining-arrays-and-objects)
      - [Task 10: Write a function to add a new person to the array of people and return the updated array.](#task-10-write-a-function-to-add-a-new-person-to-the-array-of-people-and-return-the-updated-array)
  - [Achievement](#achievement)

# Day 6: Arrays and Objects

## Tasks/Activities

### Activity 1: Arrays

#### Task 1: Create an array of numbers and log the array to the console.

```javascript
const numbers = [1, 2, 3, 4, 5];
console.log(numbers);
```

**Explanation:** This code creates an array named `numbers` containing five elements and logs the array to the console.

#### Task 2: Write a function to find the sum of all elements in an array and return the result.

```javascript
function sumArray(arr) {
  return arr.reduce((sum, current) => sum + current, 0);
}

// Example usage:
console.log(sumArray(numbers)); // Output: 15
```

**Explanation:** This function uses the `reduce` method to sum all elements in the array. The `reduce` method iterates over each element, accumulating the sum.

#### Task 3: Write a function to find the maximum element in an array and return the result.

```javascript
function findMax(arr) {
  return Math.max(...arr);
}

// Example usage:
console.log(findMax(numbers)); // Output: 5
```

**Explanation:** This function uses the `Math.max` method along with the spread operator (`...`) to find the maximum element in the array.

### Activity 2: Objects

#### Task 4: Create an object representing a person with properties for name, age, and city. Log the object to the console.

```javascript
const person = {
  name: 'John Doe',
  age: 30,
  city: 'New York'
};
console.log(person);
```

**Explanation:** This code creates an object named `person` with properties `name`, `age`, and `city`, and logs the object to the console.

#### Task 5: Write a function to log a greeting message using the properties of the person object.

```javascript
function greetPerson(person) {
  console.log(`Hello, my name is ${person.name}, I am ${person.age} years old and I live in ${person.city}.`);
}

// Example usage:
greetPerson(person); // Output: Hello, my name is John Doe, I am 30 years old and I live in New York.
```

**Explanation:** This function takes a `person` object as input and logs a greeting message using the object's properties.

### Activity 3: Array of Objects

#### Task 6: Create an array of objects representing different people, each with properties for name, age, and city. Log the array to the console.

```javascript
const people = [
  { name: 'Alice', age: 25, city: 'Los Angeles' },
  { name: 'Bob', age: 28, city: 'Chicago' },
  { name: 'Charlie', age: 35, city: 'San Francisco' }
];
console.log(people);
```

**Explanation:** This code creates an array named `people` containing three objects, each representing a person with properties `name`, `age`, and `city`, and logs the array to the console.

#### Task 7: Write a function to find the person with the maximum age in the array and return the person's object.

```javascript
function findOldestPerson(people) {
  return people.reduce((oldest, current) => (current.age > oldest.age ? current : oldest), people[0]);
}

// Example usage:
console.log(findOldestPerson(people)); // Output: { name: 'Charlie', age: 35, city: 'San Francisco' }
```

**Explanation:** This function uses the `reduce` method to iterate over the array of people and find the person with the maximum age.

### Activity 4: Array Methods

#### Task 8: Write a function to filter the array of people to only include those who live in a specific city and return the filtered array.

```javascript
function filterByCity(people, city) {
  return people.filter(person => person.city === city);
}

// Example usage:
console.log(filterByCity(people, 'Chicago')); // Output: [{ name: 'Bob', age: 28, city: 'Chicago' }]
```

**Explanation:** This function uses the `filter` method to create a new array containing only the people who live in the specified city.

#### Task 9: Write a function to sort the array of people by age in ascending order and return the sorted array.

```javascript
function sortByAge(people) {
  return people.slice().sort((a, b) => a.age - b.age);
}

// Example usage:
console.log(sortByAge(people)); 
// Output: 
// [
//   { name: 'Alice', age: 25, city: 'Los Angeles' },
//   { name: 'Bob', age: 28, city: 'Chicago' },
//   { name: 'Charlie', age: 35, city: 'San Francisco' }
// ]
```

**Explanation:** This function uses the `slice` method to create a shallow copy of the array and then sorts the copy by age in ascending order using the `sort` method.

### Activity 5: Combining Arrays and Objects

#### Task 10: Write a function to add a new person to the array of people and return the updated array.

```javascript
function addPerson(people, newPerson) {
  return [...people, newPerson];
}

// Example usage:
const newPerson = { name: 'David', age: 22, city: 'Miami' };
console.log(addPerson(people, newPerson)); 
// Output: 
// [
//   { name: 'Alice', age: 25, city: 'Los Angeles' },
//   { name: 'Bob', age: 28, city: 'Chicago' },
//   { name: 'Charlie', age: 35, city: 'San Francisco' },
//   { name: 'David', age: 22, city: 'Miami' }
// ]
```

**Explanation:** This function uses the spread operator (`...`) to add a new person to the array of people and returns the updated array.

## Achievement

By the end of these activities, students will:

- Understand and manipulate arrays and objects in JavaScript.
- Use array methods such as `reduce`, `filter`, and `sort` to perform operations on arrays.
- Create and manipulate objects and arrays of objects.
- Combine arrays and objects to solve common problems.
- Enhance code reusability and organization using functions.
