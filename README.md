# JavaScript Basics - Complete Guide

## Table of Contents
1. [Variables and Data Types](#variables-and-data-types)
2. [Operators](#operators)
3. [Conditional Statements](#conditional-statements)
4. [Loops](#loops)
5. [Functions](#functions)
6. [Object-Oriented Programming](#object-oriented-programming)
7. [Data Structures](#data-structures)

---

## Variables and Data Types

### Declaring Variables

JavaScript provides three ways to declare variables:

- **`var`** - Old way (function-scoped, avoid in modern code)
- **`let`** - Modern way for variables that can change
- **`const`** - Modern way for variables that cannot be reassigned

```javascript
let age = 25;        // Can be changed
age = 30;            // Valid

const pi = 3.14;     // Cannot be changed
// pi = 3.14159;     // Error!
```

### Primitive Data Types

JavaScript has several primitive data types:

- **String**: Text data enclosed in quotes
- **Number**: Numeric values (integers and decimals)
- **Boolean**: True or false values
- **Undefined**: Variable declared but not assigned
- **Null**: Intentional absence of value

```javascript
let name = "Amanda";          // String
let age = 42;                 // Number
let isStudent = true;         // Boolean
let notAssigned;              // Undefined
let empty = null;             // Null
```

Use `typeof` to check a variable's data type:

```javascript
console.log(typeof name);     // "string"
console.log(typeof age);      // "number"
```

---

## Operators

### Arithmetic Operators

Perform mathematical calculations:

```javascript
let a = 10, b = 3;

console.log(a + b);   // 13 (Addition)
console.log(a - b);   // 7  (Subtraction)
console.log(a * b);   // 30 (Multiplication)
console.log(a / b);   // 3.33 (Division)
console.log(a % b);   // 1  (Modulus - remainder)
```

### Assignment Operators

Assign values to variables with shortcuts:

```javascript
let c = 10;
c += 5;    // c = c + 5  → 15
c -= 3;    // c = c - 3  → 12
```

### Comparison Operators

Compare values and return boolean results:

```javascript
console.log(5 == 5);    // true  (equal)
console.log(5 != 3);    // true  (not equal)
console.log(5 > 3);     // true  (greater than)
console.log(5 < 3);     // false (less than)
console.log(5 >= 5);    // true  (greater or equal)
```

### Logical Operators

Combine multiple conditions:

```javascript
let x = 10, y = 20;

console.log(x > 5 && y < 30);   // true (AND - both true)
console.log(x > 15 || y < 30);  // true (OR - at least one true)
console.log(!(x > 5));          // false (NOT - inverts)
```

---

## Conditional Statements

Control program flow based on conditions.

### If Statement

```javascript
let temperature = 30;

if (temperature > 25) {
    console.log('It is a hot day');
}
```

### If-Else Statement

```javascript
if (temperature > 25) {
    console.log('It is a hot day');
} else {
    console.log('It is a cold day');
}
```

### If-Else If-Else (Nested)

```javascript
if (temperature > 30) {
    console.log('Very hot');
} else if (temperature > 20) {
    console.log('Hot');
} else {
    console.log('Cold');
}
```

**Example: Grading System**

```javascript
let marks = 85;

if (marks >= 90 && marks <= 100) {
    console.log('Grade A');
} else if (marks >= 80 && marks < 90) {
    console.log('Grade B');
} else if (marks >= 70 && marks < 80) {
    console.log('Grade C');
} else if (marks >= 60 && marks < 70) {
    console.log('Grade D');
} else if (marks >= 0 && marks < 60) {
    console.log('Grade F');
} else {
    console.log('Invalid marks');
}
```

---

## Loops

Execute code repeatedly.

### For Loop

Use when you know the number of iterations:

```javascript
for (let i = 1; i <= 5; i++) {
    console.log('Count:', i);
}
// Output: 1, 2, 3, 4, 5
```

### While Loop

Use when iterations depend on a condition:

```javascript
let j = 1;
while (j <= 5) {
    console.log('Count:', j);
    j++;
}
```

### Do-While Loop

Executes at least once, then checks condition:

```javascript
let k = 1;
do {
    console.log('Count:', k);
    k++;
} while (k <= 5);
```

### Break and Continue

- **`break`**: Exit the loop entirely
- **`continue`**: Skip current iteration

```javascript
for (let m = 1; m <= 10; m++) {
    if (m === 6) {
        continue;  // Skip 6
    }
    console.log(m);  // Prints 1-5, 7-10
}
```

---

## Functions

Reusable blocks of code.

### Basic Function

```javascript
function greeting() {
    console.log("Hello World");
}

greeting();  // Call the function
```

### Function with Parameters

```javascript
function addNumbers(n1, n2) {
    console.log(n1 + n2);
}

addNumbers(10, 20);  // Output: 30
```

### Function with Return Value

```javascript
function multiply(a, b) {
    return a * b;
}

let result = multiply(5, 4);
console.log(result);  // Output: 20
```

**Example: Calculator Function**

```javascript
function calculator(n1, n2, operator) {
    if (operator === '+') {
        return n1 + n2;
    } else if (operator === '-') {
        return n1 - n2;
    } else if (operator === '*') {
        return n1 * n2;
    } else if (operator === '/') {
        return n1 / n2;
    } else {
        return 'Invalid operator';
    }
}

console.log(calculator(10, 5, '+'));  // 15
console.log(calculator(10, 5, '*'));  // 50
```

---

## Object-Oriented Programming

### Classes and Objects

A **class** is a blueprint, an **object** is an instance.

```javascript
class Car {
    display() {
        console.log('This is a car');
    }
}

const myCar = new Car();
myCar.display();  // "This is a car"
```

### Constructor

Initialize object properties:

```javascript
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }
    
    greet() {
        console.log(`Hi, I'm ${this.name}`);
    }
}

const person1 = new Person('Alice', 25);
person1.greet();  // "Hi, I'm Alice"
```

**Example: ATM Class**

```javascript
class ATM {
    constructor(accountNumber, pin, balance) {
        this.accountNumber = accountNumber;
        this.pin = pin;
        this.balance = balance;
    }
    
    checkBalance() {
        return this.balance;
    }
    
    deposit(amount) {
        this.balance += amount;
        console.log(`Deposited: ${amount}`);
    }
    
    withdraw(amount) {
        if (amount > this.balance) {
            console.log('Insufficient balance');
        } else {
            this.balance -= amount;
            console.log(`Withdrawn: ${amount}`);
        }
    }
}

const customer = new ATM('123456', '1234', 1000);
customer.deposit(500);   // Balance: 1500
customer.withdraw(300);  // Balance: 1200
```

### Inheritance

Child class inherits from parent class:

```javascript
class Parent {
    constructor(name) {
        this.name = name;
    }
    
    speak() {
        console.log(`${this.name} is speaking`);
    }
}

class Child extends Parent {
    constructor(name, age) {
        super(name);  // Call parent constructor
        this.age = age;
    }
    
    play() {
        console.log(`${this.name} is playing`);
    }
}

const child = new Child('Bobby', 10);
child.speak();  // Inherited method
child.play();   // Own method
```

---

## Data Structures

### Arrays

Store multiple values of the same type:

```javascript
const numbers = [1, 2, 3, 4, 5];

console.log(numbers[0]);     // Access: 1
numbers.push(6);             // Add: [1,2,3,4,5,6]
numbers.pop();               // Remove last: [1,2,3,4,5]
console.log(numbers.length); // Size: 5
```

### Objects

Store key-value pairs:

```javascript
const student = {
    id: 101,
    name: "Kalisa",
    age: 20,
    isEnrolled: true
};

console.log(student.name);       // Access: "Kalisa"
console.log(student.isEnrolled); // Access: true
```

---

## Best Practices

1. Use `const` by default, `let` when you need to reassign
2. Use meaningful variable names
3. Write comments to explain complex logic
4. Keep functions small and focused
5. Use proper indentation for readability

---

## Additional Resources

- [MDN JavaScript Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)
- [JavaScript.info](https://javascript.info/)
- Practice regularly on platforms like CodeWars or LeetCode

Happy Coding! 🚀
