2023-04-30 18:54
Status: #Documentation 
Tags: [[React]]

# Class Components

* When react is rendering and re-rendering your website
* We are going to write things in class components or functional components, with the modern version being functional components
* We mainly want to tell React when we want to render and re-render different parts of the website

* Something is done rendering as soon as the user can interact with it
* JSX is a syntax extension of JavaScript

## First example of a class component


```javascript
import { Component } from 'react';

  

import logo from './logo.svg';

import './App.css';

  

class App extends Component {

  // function App() {

  render() {

    return (

      <div className="App" >

        <header className="App-header">

          <img src={logo} className="App-logo" alt="logo" />

          <p>

            Hello my name is Liam.

          </p>

          <a

            className="App-link"

            href="https://reactjs.org"

            target="_blank"

            rel="noopener noreferrer"

          >

            Learn React

          </a>

        </header>

      </div>

    );

  }

  

}

  

export default App;
```








___
# Flashcards



---
# References
