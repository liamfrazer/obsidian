2023-05-03 17:16
Status: #Documentation 
Tags: [[React]]

# componentDidMount

* https://jsonplaceholder.typicode.com/users
* We need to understand where we're going to put this data
* We need to update the state of monsters once we've retrieved the information from the API
* The application shouldn't need to worry about how much data, except being empty
* If the API request fails in the middle, they should just see the empty array during a failure
* We need to understand the empty case

* How do I get the list? When do I get the list? Where do I put the list?

* This is where React provides us with Lifecycle methods
* We want to re-render the app, we want the data the moment its rendered by React

* Most important `component features`

```javascript
componentDidCatch?
componentDidMount?
componentDidUpdate?
ComponentWillUnmount?
```

* componentDidMount() is a method we have access
* Whatever code sits inside `componentDidMount` runs the moment the component is loaded
* Mounting is the first time the component is on the DOM
* This only happens once, the only re-mount is once its re-mounted, technically a different component

* A promise is async in JavaScript, JavaScript fetches the data, if succussed it will come back

* Every .then is going to return a Promise that has been resolved


```javascript
  componentDidMount() {
    fetch('https://jsonplaceholder.typicode.com/users')
      .then(response => response.json())
  }
```


```javascript
  componentDidMount() {
    fetch('https://jsonplaceholder.typicode.com/users')
      .then(response => response.json())
      .then((users) => this.setState(() => {
        return { monsters: users }
      }, () => {
        console.log(this.state);
      }))
  }
```

* Whenever we have a class component, that uses a API, this should be used within componentDidMount()

* Chat GPT


___
# Flashcards



---
# References
