# Day 16: Recursion

## Tasks/Activities

### Activity 1: Basic Recursion

#### Task 1: Write a recursive function to calculate the factorial of a number. Log the result for a few test cases.

```javascript
const factorial = (n) => {
    if (n == 1 || n == 0) return 1;
    return factorial(n - 1) * n;
}

// Test cases
console.log(factorial(5)); // Output: 120
console.log(factorial(7)); // Output: 5040
```

#### Task 2: Write a recursive function to calculate the nth Fibonacci number. Log the result for a few test cases.

```javascript
function fibonacci(n) {
  if (n <= 1) {
    return n;
  } else {
    return fibonacci(n - 1) + fibonacci(n - 2);
  }
}

// Test cases
console.log(fibonacci(6)); // Output: 8
console.log(fibonacci(10)); // Output: 55
```

### Activity 2: Recursion with Arrays

#### Task 3: Write a recursive function to find the sum of all elements in an array. Log the result for a few test cases.

```javascript
const sumArray = (arr) => {
    let sum = 0;

    if (Array.isArray(arr)) {
        for (let i = 0; i < arr.length; i++) {
            sum += sumArray(arr[i])
        }
    } else {
        sum += arr;
    }
    return sum;
}

// Test cases
console.log(sumArray([1, 2, 3, 4, 5])); // Output: 15
console.log(sumArray([10, 20, 30, 40])); // Output: 100
```

#### Task 4: Write a recursive function to find the maximum element in an array. Log the result for a few test cases.

```javascript
const findMaximum = (arr) => {
    let maxNum = -Infinity;
    if (Array.isArray(arr)) {
        for (let i = 0; i < arr.length; i++) {
            let currentMax = findMaximum(arr[i]);
            maxNum = (currentMax > maxNum) ? currentMax : maxNum
        }
    } else {
        maxNum = (arr > maxNum) ? arr : maxNum
    }
    return maxNum;
}
console.log(findMaximum([1, 5, 3, 9, 2])); // Output: 9
console.log(findMaximum([10, 20, 30, 40])); // Output: 40
```

### Activity 3: String Manipulation with Recursion

#### Task 5: Write a recursive function to reverse a string. Log the result for a few test cases.

```javascript
function reverseString(str) {
  if (str === "") {
    return "";
  } else {
    return reverseString(str.substr(1)) + str.charAt(0);
  }
}

// Test cases
console.log(reverseString("hello")); // Output: "olleh"
console.log(reverseString("world")); // Output: "dlrow"
```

#### Task 6: Write a recursive function to check if a string is a palindrome. Log the result for a few test cases.

```javascript
function isPalindrome(str) {
  if (str.length <= 1) {
    return true;
  } else if (str.charAt(0) !== str.charAt(str.length - 1)) {
    return false;
  } else {
    return isPalindrome(str.substr(1, str.length - 2));
  }
}

// Test cases
console.log(isPalindrome("madonna")); // Output: false
console.log(isPalindrome("racecar")); // Output: true
```

### Activity 4: Recursive Search

#### Task 7: Write a recursive function to perform a binary search on a sorted array. Log the index of the target element for a few test cases.

```javascript
function binarySearch(arr, target, low = 0, high = arr.length - 1) {
  if (low > high) {
    return -1;
  }
  let mid = Math.floor((low + high) / 2);
  if (arr[mid] === target) {
    return mid;
  } else if (arr[mid] > target) {
    return binarySearch(arr, target, low, mid - 1);
  } else {
    return binarySearch(arr, target, mid + 1, high);
  }
}

// Test cases
console.log(binarySearch([1, 2, 3, 4, 5, 6, 7], 5)); // Output: 4
console.log(binarySearch([10, 20, 30, 40, 50], 25)); // Output: -1
```

#### Task 8: Write a recursive function to count the occurrences of a target element in an array. Log the result for a few test cases.

```javascript
let recursiveCountOccurance = (arr, target, index = 0) => {
  if (index === arr.length) return 0;
  let count = arr[index] === target ? 1 : 0;
  return count + recursiveCountOccurance(arr, target, index + 1);
};

// Test cases
console.log(countOccurrences([1, 2, 3, 2, 2, 4, 2], 2)); // Output: 4
console.log(countOccurrences([10, 20, 30, 40, 50], 25)); // Output: 0
```

### Activity 5: Tree Traversal (Optional)

#### Task 9: Write a recursive function to perform an in-order traversal of a binary tree. Log the nodes as they are visited.

```javascript
class TreeNode {
  constructor(value) {
    this.value = value;
    this.left = null;
    this.right = null;
  }
}

function inOrderTraversal(node) {
  if (node !== null) {
    inOrderTraversal(node.left);
    console.log(node.value);
    inOrderTraversal(node.right);
  }
}

// Example usage
let root = new TreeNode(1);
root.left = new TreeNode(2);
root.right = new TreeNode(3);
root.left.left = new TreeNode(4);
root.left.right = new TreeNode(5);

inOrderTraversal(root); // Output: 4 2 5 1 3
```

#### Task 10: Write a recursive function to calculate the depth of a binary tree. Log the result for a few test cases.

```javascript
function treeDepth(node) {
  if (node === null) {
    return 0;
  } else {
    let leftDepth = treeDepth(node.left);
    let rightDepth = treeDepth(node.right);
    return Math.max(leftDepth, rightDepth) + 1;
  }
}

// Example usage
console.log(treeDepth(root)); // Output: 3
```

## Feature Request

### 1. Factorial and Fibonacci Script

```javascript
function factorial(n) {
  if (n === 0) {
    return 1;
  } else {
    return n * factorial(n - 1);
  }
}

function fibonacci(n) {
  if (n <= 1) {
    return n;
  } else {
    return fibonacci(n - 1) + fibonacci(n - 2);
  }
}
```

### 2. Array Recursion Script

```javascript
function sumArray(arr, n) {
  if (n <= 0) {
    return 0;
  } else {
    return sumArray(arr, n - 1) + arr[n - 1];
  }
}

function maxArray(arr, n) {
  if (n === 1) {
    return arr[0];
  } else {
    return Math.max(arr[n - 1], maxArray(arr, n - 1));
  }
}
```

### 3. String Recursion Script

```javascript
function reverseString(str) {
  if (str === "") {
    return "";
  } else {
    return reverseString(str.substr(1)) + str.charAt(0);
  }
}

function isPalindrome(str) {
  if (str.length <= 1) {
    return true;
  } else if (str.charAt(0) !== str.charAt(str.length - 1)) {
    return false;
  } else {
    return isPalindrome(str.substr(1, str.length - 2));
  }
}
```

### 4. Recursive Search Script

```javascript
function binarySearch(arr, target, low = 0, high = arr.length - 1) {
  if (low > high) {
    return -1;
  }
  let mid = Math.floor((low + high) / 2);
  if (arr[mid] === target) {
    return mid;
  } else if (arr[mid] > target) {
    return binarySearch(arr, target, low, mid - 1);
  } else {
    return binarySearch(arr, target, mid + 1, high);
  }
}

function countOccurrences(arr, target, index = 0) {
  if (index === arr.length) {
    return 0;
  }
  let count = arr[index] === target ? 1 : 0;
  return count + countOccurrences(arr, target, index + 1);
}
```

### 5. Tree Traversal Script

```javascript
class TreeNode {
  constructor(value) {
    this.value = value;
    this.left = null;
    this.right = null;
  }
}

function inOrderTraversal(node) {
  if (node !== null) {
    inOrderTraversal(node.left);
    console.log(node.value);
    inOrderTraversal(node.right);
  }
}

function treeDepth(node) {
  if (node === null) {
    return 0;
  } else {
    let leftDepth = treeDepth(node.left);
    let rightDepth = treeDepth(node.right);
    return Math.max(leftDepth, rightDepth) + 1;
  }
}
```

## Achievement

By the end of these activities, students will:

1. Understand and implement basic recursion.
2. Apply recursion to solve problems with arrays and strings.
3. Use recursion for searching and counting elements in arrays.
4. Perform tree traversal and calculate tree depth using recursion (optional).
