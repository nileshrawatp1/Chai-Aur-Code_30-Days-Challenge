# Table Of Content

- [Table Of Content](#table-of-content)
- [Day 14: Classes](#day-14-classes)
  - [Tasks/Activities](#tasksactivities)
    - [Activity 1: Class Definition](#activity-1-class-definition)
    - [Activity 2: Class Inheritance](#activity-2-class-inheritance)
    - [Activity 3: Static Methods and Properties](#activity-3-static-methods-and-properties)
    - [Activity 4: Getters and Setters](#activity-4-getters-and-setters)
    - [Activity 5: Private Fields (Optional)](#activity-5-private-fields-optional)
  - [Achievements](#achievements)

# Day 14: Classes

## Tasks/Activities

### Activity 1: Class Definition

**Task 1: Define a class `Person` with properties `name` and `age`, and a method to return a greeting message. Create an instance of the class and log the greeting message.**

```javascript
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }

    // Method to return a greeting message
    greeting() {
        return `Hello, my name is ${this.name} and I am ${this.age} years old.`;
    }
}

// Create an instance of the class
const person1 = new Person('Nilesh', 29);
console.log(person1.greeting()); // Output: Hello, my name is Nilesh and I am 29 years old.
```

**Task 2: Add a method to the `Person` class that updates the age property and logs the updated age.**

```javascript
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }

    // Method to return a greeting message
    greeting() {
        return `Hello, my name is ${this.name} and I am ${this.age} years old.`;
    }

    // Method to update the age and log the updated age
    updateAge(newAge) {
        this.age = newAge;
        console.log(`Updated Age: ${this.age}`);
    }
}

// Create an instance of the class
const person2 = new Person('kapil', 28);
person2.updateAge(26); // Output: Updated Age: 28
```

### Activity 2: Class Inheritance

**Task 3: Define a class `Student` that extends the `Person` class. Add a property `studentId` and a method to return the student ID. Create an instance of the `Student` class and log the student ID.**

```javascript
class Student extends Person {
    constructor(name, age, studentId) {
        super(name, age);
        this.studentId = studentId;
    }

    // Method to return the student ID
    getStudentId() {
        return this.studentId;
    }
}

// Create an instance of the Student class
const student1 = new Student('Aakash', 25, 'A251999');
console.log(`Student ID: ${student1.getStudentId()}`); // Output: Student ID: A251999
```

**Task 4: Override the greeting method in the `Student` class to include the student ID in the message. Log the overridden greeting message.**

```javascript
class Student extends Person {
    constructor(name, age, studentId) {
        super(name, age);
        this.studentId = studentId;
    }

    // Method to return the student ID
    getStudentId() {
        return this.studentId;
    }

    // Override the greeting method to include the student ID
    greeting() {
        return `Hello, my name is ${this.name}, I am ${this.age} years old, and my student ID is ${this.studentId}.`;
    }
}

// Create an instance of the Student class
const student2 = new Student('Nilesh', 29, 'N261995');
console.log(student2.greeting()); // Output: Hello, my name is Nilesh, I am 29 years old, and my student ID is N261995.
```

### Activity 3: Static Methods and Properties

**Task 5: Add a static method to the `Person` class that returns a generic greeting message. Call this static method without creating an instance of the class and log the message.**

```javascript
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }

    // Method to return a greeting message
    greeting() {
        return `Hello, my name is ${this.name} and I am ${this.age} years old.`;
    }

    // Method to update the age and log the updated age
    updateAge(newAge) {
        this.age = newAge;
        console.log(`Updated Age: ${this.age}`);
    }

    // Static method to return a generic greeting message
    static genericGreeting() {
        return "Hello, this is a generic greeting from the Person class.";
    }
}

// Call the static method without creating an instance of the class
console.log(Person.genericGreeting()); // Output: Hello, this is a generic greeting from the Person class.
```

**Task 6: Add a static property to the `Student` class to keep track of the number of students created. Increment this property in the constructor and log the total number of students.**

```javascript
class Student extends Person {
    static studentCount = 0;

    constructor(name, age, studentId) {
        super(name, age);
        this.studentId = studentId;
        Student.studentCount++; // Increment the student count
    }

    // Method to return the student ID
    getStudentId() {
        return this.studentId;
    }

    // Override the greeting method to include the student ID
    greeting() {
        return `Hello, my name is ${this.name}, I am ${this.age} years old, and my student ID is ${this.studentId}.`;
    }

    // Static method to return the current student count
    static getStudentCount() {
        return Student.studentCount;
    }
}

// Create instances of the Student class
const student3 = new Student('Nilesh', 29, 'N261995');
const student4 = new Student('Kapil', 28, 'K131996');
console.log(Student.getStudentCount()); // Output: 2
```

### Activity 4: Getters and Setters

**Task 7: Add a getter method to the `Person` class to return the full name (assume a `firstName` and `lastName` property). Create an instance and log the full name using the getter.**

```javascript
class Person {
    constructor(firstName, lastName, age) {
        this.firstName = firstName;
        this.lastName = lastName;
        this.age = age;
    }

    // Getter method to return the full name
    get fullName() {
        return `${this.firstName} ${this.lastName}`;
    }

    // Method to return a greeting message
    greeting() {
        return `Hello, my name is ${this.firstName} ${this.lastName} and I am ${this.age} years old.`;
    }

    // Method to update the age and log the updated age
    updateAge(newAge) {
        this.age = newAge;
        console.log(`Updated Age: ${this.age}`);
    }
}

// Create an instance of the class
const person3 = new Person('Nilesh', 'Rawat', 29);
console.log(`Full Name: ${person3.fullName}`); // Output: Full Name: Nilesh Rawat
```

**Task 8: Add a setter method to the `Person` class to update the name properties (`firstName` and `lastName`). Update the name using the setter and log the updated full name.**

```javascript
class Person {
    constructor(firstName, lastName, age) {
        this.firstName = firstName;
        this.lastName = lastName;
        this.age = age;
    }

    // Getter method to return the full name
    get fullName() {
        return `${this.firstName} ${this.lastName}`;
    }

    // Setter method to update the full name
    set fullName(name) {
        const [firstName, lastName] = name.split(' ');
        this.firstName = firstName;
        this.lastName = lastName;
    }

    // Method to return a greeting message
    greeting() {
        return `Hello, my name is ${this.firstName} ${this.lastName} and I am ${this.age} years old.`;
    }

    // Method to update the age and log the updated age
    updateAge(newAge) {
        this.age = newAge;
        console.log(`Updated Age: ${this.age}`);
    }
}

// Create an instance of the class
const person4 = new Person('Nilesh', 'Rawat', 29);
person4.fullName = 'Emily Johnson'; // Use the setter method to update the name
console.log(`Updated Full Name: ${person4.fullName}`); // Output: Updated Full Name: Nilesh Rawat
```

### Activity 5: Private Fields (Optional)

**Task 9: Define a class `Account` with private fields for `balance` and a method to deposit and withdraw money. Ensure that the balance can only be updated through these methods.**

```javascript
class Account {
    #balance;

    constructor(initialBalance) {
        this.#balance = initialBalance;
    }

    // Method to deposit money
    deposit(amount) {
        if (amount > 0) {
            this.#balance += amount;
            console.log(`Deposited: ${amount}, New Balance: ${this.#balance}`);
        } else {
            console.log('Deposit amount must be positive.');
        }
    }

    // Method to withdraw money
    withdraw(amount) {
        if (amount > 0 && amount <= this.#balance) {
            this.#balance -= amount;
            console.log(`Withdrew: ${amount}, New Balance: ${this.#balance}`);
        } else {
            console.log('Invalid withdraw amount.');
        }
    }

    // Method to get the balance
    getBalance() {
        return this.#balance;
    }
}

// Create an instance of the Account class
const account1 = new Account(1000);
account1.deposit(500); // Output: Deposited: 500, New Balance: 1500
account1.withdraw(200); // Output: Withdrew: 200, New Balance: 1300
console.log(`Current Balance: ${account1.getBalance()}`); // Output: Current Balance: 1300
```

**Task 10: Create an instance of the `Account` class and test the deposit and withdraw methods, logging the balance after each operation.**

```javascript
// Creating an instance and testing deposit and withdraw methods
const account2 = new Account(2000);
account2.deposit(1000); // Output: Deposited: 1000, New Balance: 3000
account2.withdraw(500); // Output: Withdrew: 500, New Balance: 2500
account2.withdraw(3000); // Output: Invalid withdraw amount.
console.log(`Final Balance: ${account2.getBalance()}`); // Output: Final Balance: 2500
```

## Achievements

By the end of these activities, students will:
- Define and use classes with properties and methods.
- Implement inheritance to extend classes.
- Utilize static methods and properties.
- Apply getters and setters for encapsulation.
- Understand and use private fields in classes (optional).
