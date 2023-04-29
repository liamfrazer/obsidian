2023-04-29 14:34
Status: #Documentation #Video 
Tags: [[JavaScript]]

# Hypotenuse Calculator

## Window Prompt

```javascript
let a;
let b;
let c;
 
a = window.prompt("Enter side A:");
a = Number(a); // 3

b = window.prompt("Enter side B:");
b = Number(b); // 4

c = Math.sqrt(Math.pow(a, 2) + Math.pow(b, 2))

console.log("Side C:", c); // Side C: 5
```

## HTML Text Boxes

```html
<body>
    <label for="aTextBox" id="aLabel">Side A:</label></br>
    <input type="text" id="aTextBox"></br>
    <label for="bTextBox" id="bLabel">Side B:</label></br>
    <input type="text" id="bTextBox"></br>
    <button type="button" id="submitButton">Submit</button></br></br>
    <label for="cTextBox" id="cLabel">Side C:</label></br>
    <script src="index.js"></script>
</body>
```







___
# Flashcards



---
# References
[Hypotenuse Calc Practice Program](https://www.youtube.com/watch?v=8dWL3wF_OMw&list=PL3k5VlZzpQyEz03mNlmU50YcIJ6vEDz95&index=1&t=2212s)
