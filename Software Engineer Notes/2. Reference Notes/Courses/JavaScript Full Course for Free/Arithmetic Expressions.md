2023-04-29 12:22
Status: #Documentation 
Tags: [[JavaScript]]

# Arithmetic Expressions
* Arithmetic expressions is a combination of;
1. Operands (values, variables, etc..)
2. Operators (+ - * / %)
* These can then be evaluated to a value
* `y = x + 5`

```javascript
let students = 20;

students = students + 1; // 21

students = students - 1; // 19

students = students * 2; // 40

students = students / 2; // 10

let extraStudents = students % 3; // 2
```
* The modulus is `%`, it gives you the remainder of any division

## Augmented Assignment Operator
```javascript
students += 1; // 21

students -= 1; // 19

students *= 2; // 40

students /= 2; // 10
```

## Operator Precedence
1. Parenthesis ()
2. Exponents
3. Multiplication & Division
4. Addition & Subtraction

```javascript
let result = 1 + 2 * (3 + 4);
console.log(result); // 15
```

* By adding a set of Parenthesis, you can force operator precedence



___
# Flashcards



---
# References
[Arithmetic Expressions](https://www.youtube.com/watch?v=8dWL3wF_OMw&list=PL3k5VlZzpQyEz03mNlmU50YcIJ6vEDz95&index=1&t=992s)
