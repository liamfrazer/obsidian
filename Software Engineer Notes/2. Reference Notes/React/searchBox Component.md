2023-05-06 17:40
Status: #Documentation 
Tags: [[React]]

# searchBox Component

* input is meant to be a generic search box component


```javascript
            <input className='search-box' type='search' placeholder='Search...' onChange={onSearchChange}></input>
```
* We want to keep the type as Search to ensure the correct box is displayed
* We don't want to keep the className as generic, as this wouldn't be dynamic
* We want this to be more specific


```javascript
        <SearchBox onChangeHandler={onSearchChange} />
```
```javascript
<input className='search-box' type='search' placeholder='Search...' onChange={this.props.onChangeHandler}></input>
```

* 
## Final Code


```javascript
import { Component } from 'react';

  

class SearchBox extends Component {

  

    render() {

        return (

            <input

            className={this.props.className}

            type='search'

            placeholder={this.props.placeholder}

            onChange={this.props.onChangeHandler}>

            </input>

        )

    }

}

  

export default SearchBox
```

```javascript
div className="App" >

        <SearchBox

          className='monster-search-box'

          placeholder='Search...'

          onChangeHandler={onSearchChange} />

        <CardList

          monsters={filteredMonsters} />
```






___
# Flashcards



---
# References
