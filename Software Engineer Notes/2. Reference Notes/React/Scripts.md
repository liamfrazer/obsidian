2023-04-30 17:38
Status: #Documentation 
Tags: [[React]]

# Scripts

* Directly installs all the required files and then executes it immediately
* NPX downloads the latest package, then removes it
* Environment isn't clogged up

* Babel translate code to basic JavaScript
* Chunking via webhack, module being a chunk
* PWA allows users to use the website while offline
* 
* A component is a self contained piece of code returning a UI, all HTML/CSS/JS is contained within a function


```javascript
import logo from './logo.svg';
import './App.css';

function App() {
  return (
    <div className="App">
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

export default App;
```





___
# Flashcards



---
# References
