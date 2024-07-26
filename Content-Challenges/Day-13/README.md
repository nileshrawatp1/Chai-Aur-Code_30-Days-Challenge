# Table Of Content

- [Table Of Content](#table-of-content)
  - [Day 13: Modules](#day-13-modules)
    - [Activity 1: Creating and Exporting Modules](#activity-1-creating-and-exporting-modules)
    - [Activity 2: Named and Default Exports](#activity-2-named-and-default-exports)
    - [Activity 3: Importing Entire Modules](#activity-3-importing-entire-modules)
    - [Activity 4: Using Third-Party Modules](#activity-4-using-third-party-modules)
    - [Activity 5: Module Bundling (Optional)](#activity-5-module-bundling-optional)
    - [Feature Request](#feature-request)

## Day 13: Modules

### Activity 1: Creating and Exporting Modules

**Task 1: Create a module that exports a function to add two numbers. Import and use this module in another script.**

**math.js**

```javascript
export function add(a, b) {
  return a + b;
}
```

**index.js**

```javascript
import { add } from "./math.js";

console.log(add(2, 3)); // Output: 5
```

**Explanation:**

- We create a module named `math.js` that exports an `add` function.
- In `index.js`, we import the `add` function from `math.js` and use it to add two numbers.

**Task 2: Create a module that exports an object representing a person with properties and methods. Import and use this module in another script.**

**person.js**

```javascript
export const person = {
  firstName: "John",
  lastName: "Doe",
  getFullName: function () {
    return `${this.firstName} ${this.lastName}`;
  },
};
```

**index.js**

```javascript
import { person } from "./person.js";

console.log(person.getFullName()); // Output: John Doe
```

**Explanation:**

- We create a module named `person.js` that exports an object representing a person with properties and methods.
- In `index.js`, we import the `person` object from `person.js` and use its methods.

### Activity 2: Named and Default Exports

**Task 3: Create a module that exports multiple functions using named exports. Import and use these functions in another script.**

**utils.js**

```javascript
export function greet(name) {
  console.log(`Hello, ${name}!`);
}

export function sum(a, b) {
  return a + b;
}
```

**index.js**

```javascript
import { greet, sum } from "./utils.js";

greet("Alice");
console.log(sum(2, 3));
```

**Explanation:**

- We create a module named `utils.js` that exports multiple functions using named exports.
- In `index.js`, we import the `greet` and `sum` functions from `utils.js` and use them.

**Task 4: Create a module that exports a single function using default export. Import and use this function in another script.**

**calculator.js**

```javascript
export default function calculate(operator, x, y) {
  switch (operator) {
    case "+":
      return x + y;
    case "-":
      return x - y;
    case "*":
      return x * y;
    case "/":
      return x / y;
    default:
      throw new Error("Invalid operator");
  }
}
```

**index.js**

```javascript
import calculate from "./calculator.js";

console.log(calculate("+", 5, 3)); // Output: 8
```

**Explanation:**

- We create a module named `calculator.js` that exports a single function using default export.
- In `index.js`, we import the default export from `calculator.js` and use it.

### Activity 3: Importing Entire Modules

**Task 5: Create a module that exports multiple constants and functions. Import the entire module as an object in another script and use its properties.**

**constants.js**

```javascript
export const PI = 3.14159;
export const GRAVITY = 9.81;

export function areaOfCircle(radius) {
  return PI * radius * radius;
}
```

**index.js**

```javascript
import * as math from "./constants.js";

console.log(math.PI);
console.log(math.areaOfCircle(2));
```

**Explanation:**

- We create a module named `constants.js` that exports multiple constants and functions.
- In `index.js`, we import the entire module as an object using `import * as math` and access its properties.

### Activity 4: Using Third-Party Modules

**Task 6: Install a third-party module (e.g., lodash) using npm. Import and use a function from this module in a script.**

**Note:** You'll need to install lodash using `npm install lodash` before running this script.

```javascript
import { sum } from "lodash";

console.log(sum([1, 2, 3])); // Output: 6
```

**Explanation:**

- We import the `sum` function from the `lodash` library.
- We use the `sum` function to calculate the sum of an array.

**Task 7: Install a third-party module (e.g., axios) using npm. Import and use this module to make a network request in a script.**

**Note:** You'll need to install axios using `npm install axios` before running this script.

```javascript
import axios from "axios";

axios
  .get("https://api.example.com/data")
  .then((response) => {
    console.log(response.data);
  })
  .catch((error) => {
    console.error(error);
  });
```

**Explanation:**

- We import the `axios` library.
- We use `axios.get` to make a network request and handle the response.

### Activity 5: Module Bundling (Optional)

**Task 8: Use a module bundler like Webpack or Parcel to bundle multiple JavaScript files into a single file. Write a script to demonstrate the bundling process.**

**Note:** This task requires setting up Webpack or Parcel and configuring them accordingly. Refer to their respective documentation for details.

**Basic structure:**

```bash
# package.json
{
  "name": "my-project",
  "version": "1.0.0",
  "scripts": {
    "build": "webpack" // or "parcel build"
  },
  "dependencies": {
    // ...
  }
}

# webpack.config.js (or parcel.config.js)
// Configuration for the bundler
```

**Explanation:**

- A module bundler like Webpack or Parcel combines multiple JavaScript files into a single file for production.
- The configuration for the bundler is typically defined in a `webpack.config.js` or `parcel.config.js` file.

### Feature Request

**1. Basic Module Script:** (See Task 1)
**2. Named and Default Exports Script:** (See Task 3 and Task 4)
**3. Third-Party Module Script:** (See Task 6 and Task 7)
**4. Module Bundling Script:** (See Task 8, optional)

**Remember to install required dependencies (e.g., lodash, axios) using npm.**

**Note:** The module bundling task requires additional setup and configuration.
