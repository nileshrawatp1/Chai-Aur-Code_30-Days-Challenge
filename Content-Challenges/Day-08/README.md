# Table Of Content

- [Table Of Content](#table-of-content)
- [Day 8: ES6+ Features](#day-8-es6-features)
  - [Tasks/Activities](#tasksactivities)
    - [Activity 1: Template Literals](#activity-1-template-literals)
      - [Task 1: Use template literals to create a string that includes variables for a person's name and age, and log the string to the console.](#task-1-use-template-literals-to-create-a-string-that-includes-variables-for-a-persons-name-and-age-and-log-the-string-to-the-console)
      - [Task 2: Create a multi-line string using template literals and log it to the console.](#task-2-create-a-multi-line-string-using-template-literals-and-log-it-to-the-console)
    - [Activity 2: Destructuring](#activity-2-destructuring)
      - [Task 3: Use array destructuring to extract the first and second elements from an array of numbers and log them to the console.](#task-3-use-array-destructuring-to-extract-the-first-and-second-elements-from-an-array-of-numbers-and-log-them-to-the-console)
      - [Task 4: Use object destructuring to extract the title and author from a book object and log them to the console.](#task-4-use-object-destructuring-to-extract-the-title-and-author-from-a-book-object-and-log-them-to-the-console)
    - [Activity 3: Spread and Rest Operators](#activity-3-spread-and-rest-operators)
      - [Task 5: Use the spread operator to create a new array that includes all elements of an existing array plus additional elements, and log the new array to the console.](#task-5-use-the-spread-operator-to-create-a-new-array-that-includes-all-elements-of-an-existing-array-plus-additional-elements-and-log-the-new-array-to-the-console)
      - [Task 6: Use the rest operator in a function to accept an arbitrary number of arguments, sum them, and return the result.](#task-6-use-the-rest-operator-in-a-function-to-accept-an-arbitrary-number-of-arguments-sum-them-and-return-the-result)
    - [Activity 4: Default Parameters](#activity-4-default-parameters)
      - [Task 7: Write a function that takes two parameters and returns their product, with the second parameter having a default value of 1. Log the result of calling this function with and without the second parameter.](#task-7-write-a-function-that-takes-two-parameters-and-returns-their-product-with-the-second-parameter-having-a-default-value-of-1-log-the-result-of-calling-this-function-with-and-without-the-second-parameter)
    - [Activity 5: Enhanced Object Literals](#activity-5-enhanced-object-literals)
      - [Task 8: Use enhanced object literals to create an object with methods and properties, and log the object to the console.](#task-8-use-enhanced-object-literals-to-create-an-object-with-methods-and-properties-and-log-the-object-to-the-console)
      - [Task 9: Create an object with computed property names based on variables and log the object to the console.](#task-9-create-an-object-with-computed-property-names-based-on-variables-and-log-the-object-to-the-console)
  - [Feature Request Scripts](#feature-request-scripts)
    - [1. Template Literals Script](#1-template-literals-script)
    - [2. Destructuring Script](#2-destructuring-script)
    - [3. Spread and Rest Operators Script](#3-spread-and-rest-operators-script)
    - [4. Default Parameters Script](#4-default-parameters-script)
    - [5. Enhanced Object Literals Script](#5-enhanced-object-literals-script)
  - [Achievement](#achievement)

# Day 8: ES6+ Features

## Tasks/Activities

### Activity 1: Template Literals

#### Task 1: Use template literals to create a string that includes variables for a person's name and age, and log the string to the console.

```javascript
const name = "John";
const age = 30;
const message = `My name is ${name} and I am ${age} years old.`;
console.log(message); // My name is John and I am 30 years old.
```

**Explanation:**  
Template literals allow you to embed variables directly into strings using `${variable}` syntax. This makes string concatenation easier and more readable.

#### Task 2: Create a multi-line string using template literals and log it to the console.

```javascript
const multiLineString = `This is a string
that spans across
multiple lines.`;
console.log(multiLineString);

// This is a string
// that spans across
// multiple lines.
```

**Explanation:**  
Template literals also support multi-line strings, which can be created by simply pressing Enter within the backticks.

### Activity 2: Destructuring

#### Task 3: Use array destructuring to extract the first and second elements from an array of numbers and log them to the console.

```javascript
const numbers = [1, 2, 3, 4, 5];
const [first, second] = numbers;
console.log(first, second); // 1 2
```

**Explanation:**  
Array destructuring allows you to unpack values from arrays into distinct variables in a concise manner.

#### Task 4: Use object destructuring to extract the title and author from a book object and log them to the console.

```javascript
const book = {
  title: "1984",
  author: "George Orwell",
  year: 1949
};
const { title, author } = book;
console.log(title, author); // 1984 George Orwell
```

**Explanation:**  
Object destructuring allows you to unpack properties from objects into distinct variables, making the code more readable and concise.

### Activity 3: Spread and Rest Operators

#### Task 5: Use the spread operator to create a new array that includes all elements of an existing array plus additional elements, and log the new array to the console.

```javascript
const oldArray = [1, 2, 3];
const newArray = [...oldArray, 4, 5, 6]; 
console.log(newArray);  // [1, 2, 3, 4, 5, 6]
```

**Explanation:**  
The spread operator (`...`) allows you to expand an array into individual elements. This is useful for combining arrays or adding new elements.

#### Task 6: Use the rest operator in a function to accept an arbitrary number of arguments, sum them, and return the result.

```javascript
function sum(...numbers) {
  return numbers.reduce((acc, curr) => acc + curr, 0);
}
console.log(sum(1, 2, 3, 4, 5)); // 15
```

**Explanation:**  
The rest operator (`...`) allows a function to accept an indefinite number of arguments as an array. This is useful for functions that need to handle multiple parameters.

### Activity 4: Default Parameters

#### Task 7: Write a function that takes two parameters and returns their product, with the second parameter having a default value of 1. Log the result of calling this function with and without the second parameter.

```javascript
function multiply(a, b = 1) {
  return a * b;
}
console.log(multiply(5, 2)); // Output: 10
console.log(multiply(5));    // Output: 5
```

**Explanation:**  
Default parameters allow you to specify default values for function parameters. If the parameter is not provided, the default value is used.

### Activity 5: Enhanced Object Literals

#### Task 8: Use enhanced object literals to create an object with methods and properties, and log the object to the console.

```javascript
const name = "John";
const age = 30;

const person = {
  name,
  age,
  greet() {
    console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
  }
};

console.log(person);
person.greet();
```

**Explanation:**  
Enhanced object literals allow you to define objects more concisely by omitting the property value if it matches the variable name and by defining methods directly within the object.

#### Task 9: Create an object with computed property names based on variables and log the object to the console.

```javascript
const propName = "dynamicProperty";
const value = "This is a dynamic value";

const obj = {
  [propName]: value
};

console.log(obj); // { dynamicProperty: 'This is a dynamic value' }
```

**Explanation:**  
Computed property names allow you to dynamically define property names using expressions within square brackets.

## Feature Request Scripts

### 1. Template Literals Script

```javascript
const name = "Alice";
const age = 25;
const greeting = `Hello, my name is ${name} and I am ${age} years old.`;
console.log(greeting);

const multiLine = `This is a multi-line
string using template literals.`;
console.log(multiLine);

// Hello, my name is Alice and I am 25 years old.
// This is a multi-line
// string using template literals.

```

### 2. Destructuring Script

```javascript
const array = [10, 20, 30];
const [firstElement, secondElement] = array;
console.log(firstElement, secondElement); // 10 20

const car = {
  make: "Toyota",
  model: "Corolla",
  year: 2020
};
const { make, model } = car;
console.log(make, model); // Toyota Corolla
```

### 3. Spread and Rest Operators Script

```javascript
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];
const combinedArray = [...arr1, ...arr2];
console.log(combinedArray); // [1, 2, 3, 4, 5, 6]

function sumAll(...args) {
  return args.reduce((sum, current) => sum + current, 0);
}
console.log(sumAll(1, 2, 3, 4, 5)); // 15
```

### 4. Default Parameters Script

```javascript
function add(a, b = 10) {
  return a + b;
}
console.log(add(5, 15)); // Output: 20
console.log(add(5));     // Output: 15
```

### 5. Enhanced Object Literals Script

```javascript
const key = "dynamicKey";
const value = "dynamicValue";

const dynamicObject = {
  [key]: value,
  method() {
    console.log("This is a method inside an object.");
  }
};

console.log(dynamicObject); // { dynamicKey: 'dynamicValue', method: [Function: method] }
dynamicObject.method(); //This is a method inside an object.
```

## Achievement

By the end of these activities, students will:

- Understand and use template literals for string interpolation and multi-line strings.
- Apply destructuring to extract values from arrays and objects.
- Utilize spread and rest operators for array manipulation and function arguments.
- Define functions with default parameters.
- Create objects using enhanced object literals, including methods and computed property names.
