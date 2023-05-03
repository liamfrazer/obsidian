2023-05-03 16:54
Status: #Documentation 
Tags: [[React]]

# Keys for Mapping


```console
Warning: Each child in a list should have a unique "key" prop. Check the render method of `App`. See [https://reactjs.org/link/warning-keys](https://reactjs.org/link/warning-keys "https://reactjs.org/link/warning-keys") for more information. h1 App@http://localhost:3000/static/js/bundle.js:78:5
```

* A key property is a property that should be assigned to the H1
* Most projects would have a unique ID value, normal no 2 of the strings are identical
* The key value is used by React for re-rendering

```javascript
return <h1 key={monster.id}>{monster.name}</h1>
```
* The key value is used for optimisation





___
# Flashcards



---
# References
