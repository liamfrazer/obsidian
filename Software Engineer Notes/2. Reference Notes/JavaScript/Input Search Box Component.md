2023-05-04 16:14
Status: #Documentation 
Tags: [[React]]

# Input Search Box Component

* Work on functionality first before CSS is applied
* With any feature we're building, we then understand the requirements of the feature

## input field
* We need an input field
* Every HTML tag is actually a react component that JSX has already included
* React uses className instead of class, this is a syntax exstension
* class is a protected keyword, so cannot be used in JSX


```javascript
<input className='search-box' type='search' placeholder='Search...'></input>
```
* With inputs, you typically have a change handler that combines into an input
* We're mainly looking for target within the event expression

## ChatGPT
* In this implementation, we define the `handleChange` function that updates the `searchField` property of the component's state with the current input value. We then use the `filter()` method on the `monsters` array to create a new `filteredMonsters` array that only includes monsters whose `name` property contains the value of the `searchField` property. The `toLowerCase()` method is used to make the search case-insensitive.

* Finally, we use the `map()` method to render a list of `<h1>` elements for each monster in the `filteredMonsters` array.









___
# Flashcards



---
# References
