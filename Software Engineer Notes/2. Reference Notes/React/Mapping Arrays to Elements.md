2023-05-02 21:35
Status: #Documentation 
Tags: [[React]]

# Mapping Arrays to Elements

* It's common best practice to only have one app component, and the app component is then used to render the whole application

* This is an example of where DRY can be used

```javascript
      <div className="App" >
        <h1>{this.state.monster1.name}</h1>
        <h1>{this.state.monster2.name}</h1>
        <h1>{this.state.monster3.name}</h1>
      </div >
```

## .map() method
* The .map() method allows you to iterate over every single element inside an array, giving you back a new array


```javascript
      <div className="App" >
        {
          this.state.monsters.map((monster) => {
            return <h1>{monster.name}</h1>
          })
        }
      </div >
```






___
# Flashcards



---
# References
