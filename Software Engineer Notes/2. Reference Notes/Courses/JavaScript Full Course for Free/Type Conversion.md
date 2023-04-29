2023-04-29 13:02
Status: #Documentation #Video 
Tags: [[JavaScript]]

# Type Conversion

* Type conversion = Change the data type of a value to another
* Examples would be strings, numbers, Booleans
* `typeof` can display the variable type

```javascript
let age = window.prompt("How old are you?"); // User Inputs age
console.log(typeof age); // string
age = Number(age) // Convert age to a number
console.log(typeof age); // number
age += 1; // User input + 1
console.log("Happy Birthday! You Are", age, "years old"); // Age = User Input + 1
```

```console
string 
number 
Happy Birthday! You Are 23 years old
```

```javascript
let x;
let y;
let z;

x = Number("3.14");
y = String(3.14);
z = Boolean("");
  
console.log(x, typeof x); // 3.14 number
console.log(y, typeof y); // "3.14" string
console.log(z, typeof z); // false boolean
```


___
# Flashcards



---
# References
[Type Conversion](https://www.youtube.com/watch?v=8dWL3wF_OMw&list=PL3k5VlZzpQyEz03mNlmU50YcIJ6vEDz95&index=1&t=1541s)
