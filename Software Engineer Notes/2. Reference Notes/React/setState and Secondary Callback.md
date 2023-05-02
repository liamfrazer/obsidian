2023-05-02 21:00
Status: #Documentation 
Tags: [[React]]

# setState and Secondary Callback

* The shallow merge is happening asynchronously
* This can be tested with a console.log(this.state)
* React batches the different setState calls for optimal rendering


```javascript
          <button onClick={() => {

            this.setState({ name: { firstName: 'Frazer', lastName: 'Liam' } }, () => { console.log(this.state) })

          }} >

            Change Name

          </button>
```

* The follow code can also be used:


```javascript
          <button onClick={() => {

            this.setState(() => { }, () => { })

          }}
```
* The first function is an updater function
* This is used to return an object that is then used to shallow merge against state


```javascript
          <button onClick={() => {

            this.setState(() => {

              return {

                name: { firstName: 'Frazer', lastName: 'Liam' },

              }

            }, () => { })

          }}
```
* We're passing a function that returns the object we want to shallow merge, we get access to both state and props

```javascript
this.setState((state, props) => {
```
* state is equal to the current state
* This allows us to update the state based on our previous value from the current state


* The second argument/function allows us to callback, the callback just means that once the first function has finished, we're able to call back

```javascript
          <button onClick={() => {

            this.setState(() => {

              return {

                name: { firstName: 'Frazer', lastName: 'Liam' },

              }

            }, () => { console.log(this.state) })

          }}
```


```console
Object { name: {…}, company: "ZTM" }
company: "ZTM"
name: Object { firstName: "Frazer", lastName: "Liam" }
firstName: "Frazer"
lastName: "Liam"
```
* The callback function will only run once all of the state changes had been applied
* This format is the ideal/optimal way that the setState code should be used in class components
* The callback function is entirely optional if we do/don't want to use it
* 






___
# Flashcards



---
# References
