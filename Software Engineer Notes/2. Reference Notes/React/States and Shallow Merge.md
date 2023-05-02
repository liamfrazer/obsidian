2023-05-01 18:11
Status: #Documentation 
Tags: [[React]]

# States and Shallow Merge

* setState can take an object and shallow merge
* It only updates the keys for the values that are being passed to it, anything else will be retained

## Shallow merge doesn't care about previous value


```javascript
this.state = {

      name: { firstname: 'Liam', lastName: 'Frazer' },

      company: 'ZTM'
```


```javascript
Hi {this.state.name}, I work at {this.state.company}
```
* The above code creates an error as its passing through an object, the error code states that an array should be used instead

* The follow code also causes the code to be re-rendered incorrectly


```javascript
          <p>

            Hi {this.state.name.firstName} {this.state.name.lastName}, I work at {this.state.company}

          </p>

          <button onClick={() => {

            this.setState({ name: 'Frazer' });

          }}>
```

* Our code is looking for this.state.name.lastname, whereas our setState is only passing through a string
* React doesn't care with the shallow merge

* When updating state, we want to ensure we use the same type of values,


```javascript
this.setState({ name: { firstName: 'Frazer', lastName: 'Liam' } });
```



___
# Flashcards



---
# References
