2023-04-29 13:16
Status: #Documentation #Video 
Tags: [[JavaScript]]

# const

* A `const` is a variable that can't be changed once declared

```javascript
let pi = 3.14159;
let radius;
let circumference;

radius = window.prompt("Enter the radius of a circle"); // 10
radius = Number(radius);

circumference = 2 * pi * radius; // 2 * 3.14159 * 10

console.log("The circumference is: ", circumference); // 62.8318
```

```javascript
let pi = 3.14159;
let radius;
let circumference;
  
radius = window.prompt("Enter the radius of a circle"); // 10
radius = Number(radius);

pi = 420.69; // Example of someone editing the code incorrectly
circumference = 2 * pi * radius; // 2 * 420.69 * 10

console.log("The circumference is: ", circumference); // 8413.8
```
* If `pi` was declared as a `const`, this would of prevented the program from outputting an incorrect result.




___
# Flashcards



---
# References
[const](https://www.youtube.com/watch?v=8dWL3wF_OMw&list=PL3k5VlZzpQyEz03mNlmU50YcIJ6vEDz95&index=1&t=1811s)
