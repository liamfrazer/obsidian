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







___
# Flashcards



---
# References
