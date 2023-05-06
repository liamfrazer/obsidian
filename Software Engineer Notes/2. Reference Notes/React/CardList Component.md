2023-05-06 16:34
Status: #Documentation 
Tags: [[React]]

# CardList Component

* card-list.component.jsx file

```javascript
export default CardList;
```

* Exporting a component allows other files to import the code inside the export. This should be exported by default.


```javascript
import  { Component } from 'react';
class CardList extends Component {

    render() {
        return (
            <div>
                Hello, I'm the CardList Component
            </div>
        )
    }
}
export default CardList;
```

```javascript
import CardList from './components/card-list/card-list.component'
```

```javascript
<CardList />
```

* All components must be the 1 singular component
* You cannot have multiple sibling components, you must have 1 parent component
* 



___
# Flashcards



---
# References
