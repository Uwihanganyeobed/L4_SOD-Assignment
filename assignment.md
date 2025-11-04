# DSA_JavaScript Assignment

**Total Questions: 5**  
**Level: 4 SOD**

---

## Question 1: Temperature Converter (Functions & Operators)

Write a function called `convertTemperature` that takes two parameters:
- `temperature` (number)
- `unit` (string: either "C" for Celsius or "F" for Fahrenheit)

The function should:
- If unit is "C", convert Celsius to Fahrenheit using the formula: `(C × 9/5) + 32`
- If unit is "F", convert Fahrenheit to Celsius using the formula: `(F - 32) × 5/9`
- Return the converted temperature rounded to 2 decimal places

**Example:**
```javascript
console.log(convertTemperature(0, "C"));    // Output: 32
console.log(convertTemperature(100, "C"));  // Output: 212
console.log(convertTemperature(32, "F"));   // Output: 0
console.log(convertTemperature(98.6, "F")); // Output: 37
```

---

## Question 2: Even Number Counter (Loops & Conditionals)

Write a function called `countEvenNumbers` that takes two parameters:
- `start` (starting number)
- `end` (ending number)

The function should:
- Count how many even numbers exist between `start` and `end` (inclusive)
- Return the count
- Also print each even number to the console

**Example:**
```javascript
console.log(countEvenNumbers(1, 10));  
// Prints: 2, 4, 6, 8, 10
// Returns: 5

console.log(countEvenNumbers(5, 15));  
// Prints: 6, 8, 10, 12, 14
// Returns: 5
```

---

## Question 3: Student Grade Manager (Objects & Arrays)

Create a class called `Student` with the following:

**Properties:**
- `name` (string)
- `grades` (array of numbers)

**Methods:**
- `addGrade(grade)` - Adds a grade to the grades array
- `getAverage()` - Calculates and returns the average of all grades
- `getLetterGrade()` - Returns letter grade based on average:
  - A: 90-100
  - B: 80-89
  - C: 70-79
  - D: 60-69
  - F: 0-59

**Example:**
```javascript
const student1 = new Student("Alice");
student1.addGrade(85);
student1.addGrade(92);
student1.addGrade(78);

console.log(student1.getAverage());      // Output: 85
console.log(student1.getLetterGrade());  // Output: "B"
```

---

## Question 4: Shopping Cart (OOP & Methods)

Create a class called `ShoppingCart` with the following:

**Properties:**
- `items` (array to store items)
- `totalPrice` (number, starts at 0)

**Methods:**
- `addItem(name, price)` - Adds an item object `{name, price}` to the cart and updates totalPrice
- `removeItem(name)` - Removes an item by name and updates totalPrice
- `displayCart()` - Prints all items and the total price

**Example:**
```javascript
const cart = new ShoppingCart();

cart.addItem("Apple", 1.50);
cart.addItem("Bread", 2.00);
cart.addItem("Milk", 3.50);

cart.displayCart();
// Output:
// Items in cart:
// - Apple: $1.50
// - Bread: $2.00
// - Milk: $3.50
// Total: $7.00

cart.removeItem("Bread");
cart.displayCart();
// Output:
// Items in cart:
// - Apple: $1.50
// - Milk: $3.50
// Total: $5.00
```

---

## Question 5: Number Pattern Generator (Loops & Logic)

Write a function called `printPattern` that takes one parameter:
- `rows` (number of rows)

The function should print a number pattern like this:

For `printPattern(5)`:
```
1
1 2
1 2 3
1 2 3 4
1 2 3 4 5
```

For `printPattern(3)`:
```
1
1 2
1 2 3
```

**Hint:** Use nested loops - one for rows and one for printing numbers in each row.

---

## Submission Guidelines

1. Create a new JavaScript file named `assignment.js`
2. Write your solutions with clear comments explaining your logic
3. Test each function with the provided examples and additional test cases
4. Make sure your code runs without errors

## Grading Criteria

- **Correctness**: Does the code produce the expected output? (50%)
- **Code Quality**: Is the code clean, well-organized, and readable? (25%)
- **Comments**: Are there helpful comments explaining the logic? (15%)
- **Testing**: Did you test with multiple cases? (10%)

---

**Good luck! 🎯**

*Remember: If you get stuck, review the concepts in the README file and try breaking the problem into smaller steps.*
