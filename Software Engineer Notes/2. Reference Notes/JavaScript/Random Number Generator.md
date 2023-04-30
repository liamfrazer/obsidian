2023-04-29 16:14
Status: #Documentation 
Tags: [[JavaScript]]

# Random Number Generator

## Random Number
```javascript
let x = Math.random()
console.log("Number:", x); Number: 0.6190965404088449
```

## Random Dice Roll
```javascript
let x = Math.floor(Math.random() * 6) + 1;
console.log("Number:", x);
```

## Rolling 3 dice following DRY

```javascript
let roll = () => {
    let rolls = [];
    for (let i = 0; i < 4; i++) {
        let roll = Math.floor(Math.random() * 6) + 1;
        rolls.push(roll)
    }
    return rolls;
}

let [roll1, roll2, roll3] = roll();

console.log("1:", roll1);
console.log("2:", roll2);
console.log("3:", roll3);
```

```javascript
const rollBtn = document.getElementById("rollBtn");
const label1 = document.getElementById("roll1");
const label2 = document.getElementById("roll2");
const label3 = document.getElementById("roll3");

let roll1, roll2, roll3;

const roll = () => {
    let rolls = [];
    for (let i = 0; i < 4; i++) {
        let result = Math.floor(Math.random() * 6) + 1;
        rolls.push(result)
    }
    return rolls;
}

rollBtn.onclick = function () {
    [roll1, roll2, roll3] = roll();
    label1.innerHTML = roll1;
    label2.innerHTML = roll2;
    label3.innerHTML = roll3;
}
```

## 7 Number Generator & Saver

```javascript
const num1 = document.getElementById("label1");
const num2 = document.getElementById("label2");
const num3 = document.getElementById("label3");
const num4 = document.getElementById("label4");
const num5 = document.getElementById("label5");
const num6 = document.getElementById("label6");
const num7 = document.getElementById("label7");

const numberLabels = [num1, num2, num3, num4, num5, num6, num7];
const prevResults = document.getElementById("prevResultsLabel")

const rollBtn = document.getElementById("rollBtn");
const resetBtn = document.getElementById("resetBtn");

const reset = () => {
    for (let i = 0; i < numberLabels.length; i++) {
        numberLabels[i].innerHTML = "0";
        prevResults.innerHTML = "";
    }
}

const roll = () => {
    for (let i = 0; i < numberLabels.length; i++) {
        let result = Math.floor(Math.random() * 59) + 1;
        result = Number(result)    
        
        numberLabels[i].innerHTML = result;
        prevResults.innerHTML += result + " ";
    }
}

rollBtn.onclick = roll;
resetBtn.onclick = reset;

reset();
```



___
# Flashcards



---
# References
[Random Number Generator](https://www.youtube.com/watch?v=8dWL3wF_OMw&list=PL3k5VlZzpQyEz03mNlmU50YcIJ6vEDz95&index=1&t=2812s)
