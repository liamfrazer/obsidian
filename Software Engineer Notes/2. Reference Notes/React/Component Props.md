2023-05-06 16:44
Status: #Documentation 
Tags: [[React]]

# Component Props

* Props are shorthand for properties. Identical to the properties we've already used.
* We can pass through the monsters via a prop
* We can name props whatever we want, but have to match up what we're passing in to what we're expecting


```javascript
          <CardList monsters={"I am the monsters"} />
```

```javascript
console.log(this.props)
```

```console
Object { monsters: "I am the monsters" }
```

* We are destructuring in the CardList component as this allows us to use `this.props` in multiple places without complications


```javascript
        return (

            <div>

                {monsters.map(monster => (

                    <h1 key={monster.id}>{monster.name}</h1>

                ))}

            </div>
```

* 







___
# Flashcards



---
# References
