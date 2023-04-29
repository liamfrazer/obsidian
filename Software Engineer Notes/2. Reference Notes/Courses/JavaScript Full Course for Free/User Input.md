2023-04-29 12:42
Status: #Documentation 
Tags: [[JavaScript]]

# User Input

## Easy way with a window prompt

```javascript
let username = window.prompt("What's your name?");
console.log(username); // Liam
```

## Difficult way with HTML textbox

```html
<body>
    <label for="myText" id="myLabel">Enter your name:</label></br>
    <input type="text" id="myText"></br>
    <button type="button" id="myButton">Submit</button>
    <script src="index.js"></script>
</body>
```

```javascript
let username;

document.getElementById("myButton").onClick = function () {
    username = document.getElementById("myText").value;
    console.log(username);
    document.getElementById("myLabel").innerHTML = "Hello " + username;
}
```


___
# Flashcards



---
# References
[User Input](https://www.youtube.com/watch?v=8dWL3wF_OMw&list=PL3k5VlZzpQyEz03mNlmU50YcIJ6vEDz95&index=1&t=1274s)
