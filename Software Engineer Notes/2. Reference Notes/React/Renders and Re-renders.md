2023-05-04 16:09
Status: #Documentation 
Tags: [[React]]

# Renders and Re-renders

* Runs the constructor first, classes will always run constructor first
* The constructor will initialise the state
* The render runs next and determines what to show, what the UI for the component is
* The next lifecycle is the componentDidMount, which then renders the initial UI within the DOM

* The initial state of the component is displayed, then runs componentDidMount



* Render gets called when we initlise the app with constructor, and then render gets called
* setState will trigger render from calling
* Components will also re-render when props change, our components will also re-render
* When we first render our card list, we get passed an empty array, that is getting passed into Cardlist initlially
* We call setState via the compoNentDidMount
* Because React hjs new props, this triggers a re-render

* Components re-render on setState and when props gets updated
* React renders on mount and then re-renders on either setState or when new props are changing






___
# Flashcards



---
# References
