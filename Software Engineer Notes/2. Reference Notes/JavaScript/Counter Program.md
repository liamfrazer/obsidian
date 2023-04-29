2023-04-29 15:09
Status: #Documentation 
Tags: [[JavaScript]]

# Counter Program

```html
    <label for="" id="countLabel"></label></br>
    <button id="increaseBtn">Increase</button>
    <button id="decreaseBtn">Decrease</button>
    <button id="resetBtn">Reset</button>
```

```css
#countLabel {
    display: block;
    text-align: center;
    font-size: 50px;
}

button {
    display: block;
    margin: 0 auto;
}
```

```javascript
let count = 0;

function counter(number) {
    document.getElementById("countLabel").innerHTML = number;
}

document.getElementById("decreaseBtn").onclick = function () {
    counter(count -= 1);
}

document.getElementById("increaseBtn").onclick = function () {
    counter(count += 1);
}

document.getElementById("resetBtn").onclick = function () {
    counter(count = 0);
}

counter(count);
```

___
# Flashcards



---
# References
[Counter Program](https://www.youtube.com/watch?v=8dWL3wF_OMw&list=PL3k5VlZzpQyEz03mNlmU50YcIJ6vEDz95&index=1&t=2592s)
