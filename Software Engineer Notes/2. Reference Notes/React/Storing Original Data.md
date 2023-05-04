2023-05-04 17:41
Status: #Documentation 
Tags: [[React]]

# Storing Original Data

* If you're going to modify a data within a state, and if you need to go back to it, you want to actually keep the state = to the original list.
* We want to keep the original list of users and not modify the state

* We want to render the filteredMonsters list, instead of setting the state of the original list


```javascript
          const filteredMonsters = this.state.monsters.filter((monster) => {
```

```javascript
            return { monsters: filteredMonsters }
```





___
# Flashcards



---
# References
