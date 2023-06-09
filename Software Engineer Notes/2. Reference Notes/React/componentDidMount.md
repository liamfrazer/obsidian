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

* componentDidMount() is a method we have access
* Whatever code sits inside `componentDidMount` runs the moment the component is loaded
* Mounting is the first time the component is on the DOM
* This only happens once, the only re-mount is once its re-mounted, technically a different component

* A promise is async in JavaScript, JavaScript fetches the data, if succussed it will come back

* Every .then is going to return a Promise that has been resolved


```javascript
  componentDidMount() {
    fetch('https://jsonplaceholder.typicode.com/users')
      .then(response => response.json())
  }
```


```javascript
  componentDidMount() {
    fetch('https://jsonplaceholder.typicode.com/users')
      .then(response => response.json())
      .then((users) => this.setState(() => {
        return { monsters: users }
      }, () => {
        console.log(this.state);
      }))
  }
```

* Whenever we have a class component, that uses a API, this should be used within componentDidMount()

* Chat GPT

```console
This React code is using the `componentDidMount()` lifecycle method to fetch data from an external API (in this case, the JSONPlaceholder API that returns fake data) and then updating the component's state with that data.

First, it sends an HTTP GET request to the API's `/users` endpoint using the `fetch()` method, which returns a Promise that resolves with the server's response. It then uses the `response.json()` method to parse the response body as JSON and return another Promise that resolves with the parsed data.

The second `.then()` method takes the parsed JSON data (which is an array of user objects) and uses the `setState()` method to update the `monsters` state of the component with that data. It also includes a callback function that logs the updated state to the console for debugging purposes.

Overall, this code is fetching data from an external API and using it to update the state of the component, which will likely cause it to re-render with the new data displayed.
```

## DiceRoll Test


```javascript
class App extends Component {

  constructor() {

    super();

  

    this.state = {

      diceRolls: []

    }

  }

  

  render() {

    return (

      <div className="App" >

        <button className="rollBtn" onClick={() => {

          const newRoll = {

            id: this.state.diceRolls.length + 1,

            roll: Math.floor(Math.random() * 6) + 1

          };

          this.setState((prevState) => {

            return { diceRolls: [...prevState.diceRolls, newRoll] }

          }, () => { console.log(this.state); })

          // this.setState((prevState) => {

          //   return { diceRolls: [...prevState.diceRolls, newRoll] }

          // })

        }}>Roll</button>

        <button className="clearBtn" onClick={() => {

          this.setState(() => {

            return { diceRolls: [] }

          }, () => { console.log(this.state); })

        }}>Clear</button>

        {

          this.state.diceRolls.map((rolls) => {

            return <div key={rolls.id}><h1>Roll: {rolls.id}<br></br>{rolls.roll}</h1></div>

          })

        }

      </div>

    )

  }

}
```



___
# Flashcards



---
# References
