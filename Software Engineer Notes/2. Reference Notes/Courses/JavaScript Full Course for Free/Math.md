2023-04-29 14:17
Status: #Documentation 
Tags: [[JavaScript]]

# Math
* An intrinsic object that provides basic mathematics functionality and constants.
## `Math.round()`

```javascript
let x = 3.14;
x = Math.round(x);
console.log(x); // 3
```

## `Math.floor()`
* The .floor function will always round a number down
```javascript
let x = 3.99;
x = Math.floor(x);
console.log(x); // 3
```

## `Math.ceil()
* The .ceiling function will always round a number up
```javascript
let x = 3.01;
x = Math.ceil(x);
console.log(x); // 4
```

## `Math.pow(,)`
* The .pow function will raise a value to the given power
```javascript
let x = 3;
x = Math.pow(x, 2);
console.log(x); // 9
```

## `Math.sqrt()`
* The .sqrt function will provide the square root of a value

```javascript
let x = 3;
x = Math.sqrt(x);
console.log(x); // 1.74
```

## `Math.abs()
* The .abs function will provide the distance away from 0

```javascript
let x = 3;
x = Math.abs(x);
console.log(x); // 3
```

## `Math.max()` & `Math.min()`
* Returns the larger or the lower of a set of supplied values

```javascript
let x = 3;
let y = 5;
let z = 9;

let minimum;
let maximum;

minimum = Math.min(x, y, z);
maximum = Math.max(x, y, z);

console.log(minimum); // 3
console.log(maximum); // 9
```


___
# Flashcards



---
# References
[Math](https://www.youtube.com/watch?v=8dWL3wF_OMw&list=PL3k5VlZzpQyEz03mNlmU50YcIJ6vEDz95&index=1&t=1993s)
