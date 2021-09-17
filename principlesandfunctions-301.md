# Thinking in React

- What is the `single responsibility principle` and how does it apply to components? 
  - the idea that a component should only ideally do one thing
- What does it mean to build a ‘static’ version of your application?
  - a static version takes your data model and renders the UI but has no interactivity
- Once you have a static application, what do you need to add?
  - `ReactDom.render` and `props` for interactivity
- What are the three questions you can ask to determine if something is state?
  - Is it passed in from a parent via props? If so, it probably isn’t state.
  - Does it remain unchanged over time? If yes, it probably isn’t state.
  - Can you compute it based on any other state or props in your component? If so, it's not state.
- How can you identify where state needs to live?
  - Identify every component that renders something based on that state.
  - Find a common owner component (a single component above all the components that need the state in the hierarchy).
  - Either the common owner or another component higher up in the hierarchy should own the state.
  - If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.

# Higher-Order Functions

- What is a “higher-order function”?
  - a function that operates on other functions, either by taking them as arguments or by returning them
- Explore the `greaterThan` function as defined in the reading. In your own words, what is line 2 of this function doing?
  - line 2 is returning whether the number is greater than the argument
- Explain how either `map` or `reduce` operates, with regards to higher-order functions.


## Things I want to know more about