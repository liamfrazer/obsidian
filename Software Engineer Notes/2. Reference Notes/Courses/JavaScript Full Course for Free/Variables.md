2023-04-29 10:24
Status: #Documentation 
Tags: [[JavaScript]]

# Variables

* A variable is a container for storing data.
* A variable behaves as if it was the value that it contains

## Declaration & Assignment
1. Declaration (`var`, `let`, `const`)
2. Assignment (`=` assignment operator)

* In programming, you want a variable to be descriptive of what it contains
* There may be times where you need to declare a variable, but assign a value later on

## Data Types
```javascript
let firstName = 'Liam'; // String
let age = 21; // Number
let student = true; // Boolean

console.log(firstName); // Liam
console.log(age); // 22
console.log(student); // true
```

```javascript
let firstName = 'Liam';
let age = 21;
let student = true;

age = age + 1;

console.log("Hello", firstName); // Hello Liam
console.log("You are", age, "years old"); // You are 22 years old
console.log("Enrolled:", student); // Enrolled: true
```

## Changing the DOM via JS

```html
    <p id="p1"></p>
    <p id="p2"></p>
    <p id="p3"></p>
```

```javascript
document.getElementById("p1").innerHTML = "Hello " + firstName;
document.getElementById("p2").innerHTML = "You are " + age + " years old";
document.getElementById("p3").innerHTML = "Enrolled: " + student;
```

```console
Hello Liam
You are 22 years old
Enrolled: true
```


___
# Flashcards



---
# References
[Variables](https://www.youtube.com/watch?v=8dWL3wF_OMw&t=482s)
