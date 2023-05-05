2023-05-04 17:57
Status: #Documentation 
Tags: [[React]]

# Optimisations

* In our render() function, we're currently storing an anonymous function, a function that isn't stored anywhere in a variable

```javascript
onChange={(event) => {

          const searchField = event.target.value.toLowerCase()

          this.setState(() => {

            return { searchField }

          }, () => {

          })
```

* When JavaScript runs the code, JavaScript will create the function above, but will throw it away once done. 
* Every time render is being ran, the function is being re-used
* The event value will change, but the function isn't being re-written
* 





___
# Flashcards



---
# References
