# Day 16: Recursion

## Tasks/Activities

### Activity 1: Basic Recursion

#### Task 1: Write a recursive function to calculate the factorial of a number. Log the result for a few test cases.

```javascript
// note: Normally
const factorial = (n) => {
    let result = 1;
    for (let i = 1; i < n; i++) {
        result = result * (i + 1)
    }
    return result;
}
// console.log(factorial(4))
// console.log(factorial(6))

// note: Using Recursion Function 
const factorialRecursion = (n) => {
    if (n === 1) return 1;
    return n * factorialRecursion(n - 1);
}
// console.log(factorialRecursion(4))
// console.log(factorialRecursion(6))
```

#### Task 2: Write a recursive function to calculate the nth Fibonacci number. Log the result for a few test cases.

```javascript
// note: To calculate the nth number
const fibonacci = (n) => {
    if (n < 2) return n;
    return fibonacci(n - 1) + fibonacci(n - 2)
}
// console.log(fibonacci(6))

// note: Get Sequence Using loop only 
const fibonacciSeqLoop = (n) => {
    let seq = [0, 1];
    for (let i = 2; i <= n; i++) {
        seq[i] = seq[i - 1] + seq[i - 2];
    }
    return seq
}
// console.log(fibonacciSeqLoop(10)); 

// note:  Get series using Recursion function 
const fibonacciSequence = (n, seq = [0, 1]) => {
    let seqLength = seq.length - 1;
    if (seqLength < n) {
        let nxtNumber = seq[seqLength - 1] + seq[seqLength];
        seq.push(nxtNumber);
        fibonacciSequence(n, seq);
    }
    return seq;
}
// console.log(fibonacciSequence(10))
```

### Activity 2: Recursion with Arrays

#### Task 3: Write a recursive function to find the sum of all elements in an array. Log the result for a few test cases.

```javascript
// Note: Normally 
const sumElemeents = (arr) => {
    return arr.reduce((prvCallsReturnVal, currentvalue) => {
        return (prvCallsReturnVal + currentvalue)
    }, 0)
}
// console.log(sumElemeents([1, 2, 3, 4, 5]))

// Note: Recurion Function
const sumElementsRecursion = (arr, index = 0) => {
    if (index < arr.length) {
        return arr[index] + sumElementsRecursion(arr, index + 1);
    }
    return 0;
}
// console.log(sumElementsRecursion([1, 2, 3, 4, 5]))
```

#### Task 4: Write a recursive function to find the maximum element in an array. Log the result for a few test cases.

```javascript
// Note: Normally
const maxNumber = (arr) => Math.max(...arr);
// console.log(maxNumber([9, 7, 3, 1]))
// console.log(maxNumber([9, 17, 13, 21]))


// Note: Using recursion 
const maxNumberRecursion = (arr, index = 0, maxNum = 0) => {
    if (index < arr.length) {
        maxNum = (arr[index] > maxNum) ? arr[index] : maxNum;
        return maxNumberRecursion(arr, index + 1, maxNum);
    }
    return maxNum;
}
// console.log(maxNumberRecursion([9, 7, 3, 1]))
// console.log(maxNumberRecursion([9, 17, 13, 21]))
```

### Activity 3: String Manipulation with Recursion

#### Task 5: Write a recursive function to reverse a string. Log the result for a few test cases.

```javascript
//  Note: Normally 
const revString = (str) => str.split('').reverse().join('');
// console.log(revString('Hello'))

// Note: Recursion Method 
const reverseStr = (str) => {
    if (str === '') return '';
    let firstChar = str.charAt(0);
    let leftStr = str.substr(1);
    return reverseStr(leftStr) + firstChar;
}
// console.log(reverseStr('Hello')) 
```

#### Task 6: Write a recursive function to check if a string is a palindrome. Log the result for a few test cases.

```javascript
// Note: Normally 
const palidrome = (str) => {
    const reverseStr = str.split('').reverse().join('');
    return reverseStr.toLowerCase() === str.toLowerCase();
}
// console.log(palidrome('loL'))

// Note: recursion Method 
const palindromeRecursion = (str) => {
    return (str.length <= 1) ? true
        : (str.charAt(0).toLowerCase() !== str.charAt(str.length - 1).toLowerCase()) ? false
            : palindromeRecursion(str.substr(1, str.length - 2))
}
// console.log(palindromeRecursion("Lol"))
```

### Activity 4: Recursive Search

#### Task 7: Write a recursive function to perform a binary search on a sorted array. Log the index of the target element for a few test cases.

```javascript
// Note: Normal Methods 
const binarySearch = (arr, n) => arr.indexOf(n)
// console.log(binarySearch([6, 4, 8, 3, 10, 59, 33, 2], 8))

// Note: Recursion Method 
const binarySearchRecursion = (arr, target, low = 0, high = arr.length - 1) => {
    if (low > high) return -1
    const middleIndex = Math.floor((low + high) / 2)
    if (arr[middleIndex] === target) {
        return middleIndex;
    } else if (target < arr[middleIndex]) {
        return binarySearchRecursion(arr, target, low, middleIndex - 1)
    } else {
        return binarySearchRecursion(arr, target, middleIndex + 1, high);
    }
}
console.log(binarySearchRecursion([2, 3, 4, 6, 8, 10, 33, 59], 8))
```

#### Task 8: Write a recursive function to count the occurrences of a target element in an array. Log the result for a few test cases.

```javascript
// Note: Normally 
let countOccurance = (arr, target) => {
    let count = 0;
    arr.forEach((num) => {
        if (num === target) count++;
    })
    return count;
}
console.log(countOccurance([1, 2, 3, 2, 2, 4, 2], 2)); // Output: 4
console.log(countOccurance([10, 20, 30, 40, 50], 25)); // Output: 0

// Note: recursive Method 
let recursiveCountOccurance = (arr, target, index = 0) => {
    if (index === arr.length) return 0;
    let count = arr[index] === target ? 1 : 0;
    return count + recursiveCountOccurance(arr, target, index + 1);
};
//   console.log(recursiveCountOccurance([1, 2, 3, 2, 2, 4, 2], 2)); // Output: 4
//   console.log(recursiveCountOccurance([10, 20, 30, 40, 50], 25)); // Output: 0
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
