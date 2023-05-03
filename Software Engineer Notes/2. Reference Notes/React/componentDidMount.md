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

* componentDidMount() is a method we have access to



___
# Flashcards



---
# References
