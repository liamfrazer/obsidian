2023-05-04 17:23
Status: #Documentation 
Tags: [[React]]

# Searching and Filtering

## ChatGPT


```console
In this implementation, we define the `handleChange` function that updates the `searchField` property of the component's state with the current input value. We then use the `filter()` method on the `monsters` array to create a new `filteredMonsters` array that only includes monsters whose `name` property contains the value of the `searchField` property. The `toLowerCase()` method is used to make the search case-insensitive.

Finally, we use the `map()` method to render a list of `<h1>` elements for each monster in the `filteredMonsters` array.
```


```javascript

class App extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      monsters: [],
      searchField: ''
    };
  }

  componentDidMount() {
    fetch('https://jsonplaceholder.typicode.com/users')
      .then(response => response.json())
      .then(users => this.setState({ monsters: users }));
  }

  handleChange = event => {
    this.setState({ searchField: event.target.value });
  };

  render() {
    const { monsters, searchField } = this.state;
    const filteredMonsters = monsters.filter(monster =>
      monster.name.toLowerCase().includes(searchField.toLowerCase())
    );

    return (
      <div className="App">
        <input
          className="search-box"
          type="search"
          placeholder="Search..."
          onChange={this.handleChange}
        />
        {filteredMonsters.map(monster => (
          <h1 key={monster.id}>{monster.name}</h1>
        ))}
      </div>
    );
  }
}
```

* .filer() gives us back a new array containing a list of elements running a callback on the element within the array.
* * If the search string includes the search string, then include it as a true
* You want to use non-modify methods, and create a new array with the modification in
* 








___
# Flashcards



---
# References
