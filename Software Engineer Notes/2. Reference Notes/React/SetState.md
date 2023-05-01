2023-05-01 17:55
Status: #Documentation 
Tags: [[React]]

# SetState

* React JSX allows you to attach event handlers to any HTML element


```javascript
<button onClick={() => { }}>
```
* onClick is an event listener we're combining to the HTML button
* onClick is expecting a function, we want it to be called once its clicked

* React is deciding when a component needs to be re-rendered
* `this.state` is using reference by memory
* React will only update the state of the component if the object is completely changed


```javascript
const obj1 = {name: 'Liam'}
const obj2 = obj1

obj2 === obj1
```







___
# Flashcards



---
# References
