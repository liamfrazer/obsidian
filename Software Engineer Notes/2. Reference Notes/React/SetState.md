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

obj2 === obj1 // true as same object in memory

obj1.name = 'Frazer'
obj2 // {name: 'Liam'}

const obj3 = Object.assign({}, obj1)

obj3
obj1 === obj3 // false as not the same object in memory
```

* React will decide to re-render a component when state is a completely different object in memory.


```javascript
this.setState({}) // Provide an object you want to shallow merge with your current object
```
* A shallow merge, will update and change the state object


## ChatGPT
In React, `setState()` is an asynchronous operation. When you call `setState()`, React schedules an update to the component's state and re-renders the component. The new state is not immediately available after calling `setState()`. Therefore, the `console.log()` statement that you have added will still show the old state value when it is executed.

If you want to access the updated state value after calling `setState()`, you can pass a callback function as the second argument to `setState()`. This callback function will be executed after the state update is completed and the component is re-rendered. For example:

```
<button onClick={() => {
  this.setState({ name: 'Frazer' }, () => {
    console.log(this.state);
  });
}}>
  Change Name
</button>
```

By passing the `console.log()` statement as a callback function, you can ensure that it is executed after the state update is completed and the component is re-rendered, and thus it will log the updated state value.



___
# Flashcards



---
# References
