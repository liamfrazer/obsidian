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

* We needed the original state of monsters, we always want to filter from the full list
* the best place of keeping track of arrays is within the state
* We stored the value that we wanted,

```javascript
import { Component } from 'react';

  

import logo from './logo.svg';

import './App.css';

  

class App extends Component {

  constructor() {

    super();

  

    this.state = {

      monsters: [],

      searchField: ''

    };

    console.log('constructor');

  }

  

  componentDidMount() {

    console.log('componentDidMount');

    fetch('https://jsonplaceholder.typicode.com/users')

      .then(response => response.json())

      .then((users) => this.setState(() => {

        return { monsters: users }

      }, () => {

        console.log(this.state);

      }))

  }

  

  render() {

    console.log('render');

    const filteredMonsters = this.state.monsters.filter((monster) => {

      return monster.name.toLowerCase().includes(this.state.searchField)

    })

    return (

      <div className="App" >

        <input className='search-box' type='search' placeholder='Search...' onChange={(event) => {

          const searchField = event.target.value.toLowerCase()

          this.setState(() => {

            return { searchField }

          }, () => {

          })

        }}></input>

        {

          filteredMonsters.map((monster) => {

            return <div key={monster.id}><h1>{monster.name}</h1></div>

          })

        }

      </div >

    );

  }

}

  

export default App;
```




___
# Flashcards



---
# References
