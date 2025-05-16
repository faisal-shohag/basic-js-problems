# JavaScript Beginner Problems

This README contains basic JavaScript problems for beginners covering fundamental concepts including variables, data types, objects, conditional statements, arrays, strings, and operators.

## Table of Contents
1. [Variables](#variables)
2. [Data Types](#data-types)
3. [Operators](#operators)
4. [Conditional Statements](#conditional-statements)
5. [Arrays](#arrays)
6. [Strings](#strings)
7. [Objects](#objects)

## Variables

### Problem 1: Variable Declaration and Assignment
Create a variable named `temperature` and assign it the value `25`. Then display it in the console.

**Input:**
```javascript
// Declare and assign the variable
```

**Output:**
```
25
```

**Solution:**
```javascript
let temperature = 25;
console.log(temperature);
```

### Problem 2: Variable Reassignment
Create a variable named `username` with an initial value of "guest". Then update it to "admin" and display both the old and new values.

**Input:**
```javascript
// Original value and updated value
```

**Output:**
```
Original: guest
Updated: admin
```

**Solution:**
```javascript
let username = "guest";
console.log("Original:", username);
username = "admin";
console.log("Updated:", username);
```

## Data Types

### Problem 1: Identifying Data Types
Write code to identify the data types of different values.

**Input:**
```javascript
// Identify the data types of: 42, "Hello", true, null, undefined
```

**Output:**
```
42 is a number
Hello is a string
true is a boolean
null is an object
undefined is undefined
```

**Solution:**
```javascript
console.log("42 is a", typeof 42);
console.log("Hello is a", typeof "Hello");
console.log("true is a", typeof true);
console.log("null is a", typeof null);
console.log("undefined is", typeof undefined);
```

### Problem 2: Type Conversion
Convert a string "123" to a number and add 7 to it.

**Input:**
```javascript
// String: "123"
// Add 7 to it after conversion
```

**Output:**
```
130
```

**Solution:**
```javascript
let stringNumber = "123";
let convertedNumber = Number(stringNumber);
let result = convertedNumber + 7;
console.log(result);
```

## Operators

### Problem 1: Arithmetic Operators
Calculate the area of a rectangle with length 5 and width 3, then calculate the perimeter.

**Input:**
```javascript
// Length: 5, Width: 3
// Calculate area and perimeter
```

**Output:**
```
Area: 15
Perimeter: 16
```

**Solution:**
```javascript
let length = 5;
let width = 3;
let area = length * width;
let perimeter = 2 * (length + width);
console.log("Area:", area);
console.log("Perimeter:", perimeter);
```

### Problem 2: Comparison and Logical Operators
Check if a person is eligible for a discount. They are eligible if they are either a senior (age >= 65) or a student with good grades (isStudent = true and grade >= 80).

**Input:**
```javascript
// Case 1: Age: 70, isStudent: false, grade: 0
// Case 2: Age: 20, isStudent: true, grade: 85
// Case 3: Age: 30, isStudent: false, grade: 0
```

**Output:**
```
Case 1: Eligible for discount
Case 2: Eligible for discount
Case 3: Not eligible for discount
```

**Solution:**
```javascript
function checkDiscount(age, isStudent, grade) {
 let isSenior = age >= 65;
 let isGoodStudent = isStudent && grade >= 80;

 if (isSenior || isGoodStudent) {
 return "Eligible for discount";
 } else {
 return "Not eligible for discount";
 }
}

console.log("Case 1:", checkDiscount(70, false, 0));
console.log("Case 2:", checkDiscount(20, true, 85));
console.log("Case 3:", checkDiscount(30, false, 0));
```

## Conditional Statements

### Problem 1: Simple If-Else
Determine if a number is positive, negative, or zero.

**Input:**
```javascript
// Test with numbers: 5, -3, 0
```

**Output:**
```
5 is positive
-3 is negative
0 is zero
```

**Solution:**
```javascript
function checkNumber(num) {
 if (num > 0) {
 return num + " is positive";
 } else if (num < 0) {
 return num + " is negative";
 } else {
 return num + " is zero";
 }
}

console.log(checkNumber(5));
console.log(checkNumber(-3));
console.log(checkNumber(0));
```

### Problem 2: Switch Statement
Convert day numbers to day names (1 = Monday, 2 = Tuesday, etc.)

**Input:**
```javascript
// Test with numbers: 1, 3, 6, 9
```

**Output:**
```
Day 1 is Monday
Day 3 is Wednesday
Day 6 is Saturday
Invalid day number: 9
```

**Solution:**
```javascript
function getDayName(dayNumber) {
 let dayName;

 switch (dayNumber) {
 case 1:
 dayName = "Monday";
 break;
 case 2:
 dayName = "Tuesday";
 break;
 case 3:
 dayName = "Wednesday";
 break;
 case 4:
 dayName = "Thursday";
 break;
 case 5:
 dayName = "Friday";
 break;
 case 6:
 dayName = "Saturday";
 break;
 case 7:
 dayName = "Sunday";
 break;
 default:
 return "Invalid day number: " + dayNumber;
 }

 return "Day " + dayNumber + " is " + dayName;
}

console.log(getDayName(1));
console.log(getDayName(3));
console.log(getDayName(6));
console.log(getDayName(9));
```

## Arrays

### Problem 1: Array Creation and Access
Create an array of fruits and access specific elements.

**Input:**
```javascript
// Create array with: "Apple", "Banana", "Cherry", "Date", "Elderberry"
// Access the first, third, and last elements
```

**Output:**
```
First fruit: Apple
Third fruit: Cherry
Last fruit: Elderberry
```

**Solution:**
```javascript
let fruits = ["Apple", "Banana", "Cherry", "Date", "Elderberry"];
console.log("First fruit:", fruits[0]);
console.log("Third fruit:", fruits[2]);
console.log("Last fruit:", fruits[fruits.length - 1]);
```

### Problem 2: Array Methods
Add and remove elements from an array of numbers.

**Input:**
```javascript
// Start with array: [10, 20, 30]
// Add 40 to the end
// Add 5 to the beginning
// Remove the first element
// Remove the last element
```

**Output:**
```
Original array: [10,20,30]
After adding to end: [10,20,30,40]
After adding to beginning: [5,10,20,30,40]
After removing first: [10,20,30,40]
After removing last: [10,20,30]
```

**Solution:**
```javascript
let numbers = [10, 20, 30];
console.log("Original array:", numbers);

numbers.push(40);
console.log("After adding to end:", numbers);

numbers.unshift(5);
console.log("After adding to beginning:", numbers);

numbers.shift();
console.log("After removing first:", numbers);

numbers.pop();
console.log("After removing last:", numbers);
```

## Strings

### Problem 1: String Operations
Find the length of a string and convert its case.

**Input:**
```javascript
// String: "JavaScript is Fun"
// Find length, convert to uppercase and lowercase
```

**Output:**
```
Original string: JavaScript is Fun
Length: 17
Uppercase: JAVASCRIPT IS FUN
Lowercase: javascript is fun
```

**Solution:**
```javascript
let text = "JavaScript is Fun";
console.log("Original string:", text);
console.log("Length:", text.length);
console.log("Uppercase:", text.toUpperCase());
console.log("Lowercase:", text.toLowerCase());
```

### Problem 2: String Methods
Extract parts of a string and check if it contains a specific word.

**Input:**
```javascript
// String: "Learn JavaScript programming step by step"
// Get first 5 characters
// Get characters from position 6 to 16
// Check if it contains the word "programming"
```

**Output:**
```
First 5 characters: Learn
Characters 6-16: JavaScript
Contains "programming": true
```

**Solution:**
```javascript
let phrase = "Learn JavaScript programming step by step";
console.log("First 5 characters:", phrase.substring(0, 5));
console.log("Characters 6-16:", phrase.substring(6, 16));
console.log('Contains "programming":', phrase.includes("programming"));
```

## Objects

### Problem 1: Creating and Accessing Objects
Create a person object and access its properties.

**Input:**
```javascript
// Create an object with name, age, and city properties
// Access each property
```

**Output:**
```
Name: John Doe
Age: 25
City: New York
```

**Solution:**
```javascript
let person = {
 name: "John Doe",
 age: 25,
 city: "New York"
};

console.log("Name:", person.name);
console.log("Age:", person.age);
console.log("City:", person.city);
```

### Problem 2: Modifying Objects
Add, modify, and delete properties of an object.

**Input:**
```javascript
// Create a car object with make and model
// Add a year property
// Change the model property
// Delete the make property
```

**Output:**
```
Original car: {make: "Toyota", model: "Corolla"}
After adding year: {make: "Toyota", model: "Corolla", year: 2022}
After changing model: {make: "Toyota", model: "Camry", year: 2022}
After deleting make: {model: "Camry", year: 2022}
```

**Solution:**
```javascript
let car = {
 make: "Toyota",
 model: "Corolla"
};
console.log("Original car:", car);

// Add a property
car.year = 2022;
console.log("After adding year:", car);

// Change a property
car.model = "Camry";
console.log("After changing model:", car);

// Delete a property
delete car.make;
console.log("After deleting make:", car);
```
