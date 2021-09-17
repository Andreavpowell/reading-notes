# React Lifecycle

- `render` must always happen before `componentDidMount`
- the first thing that happens in the lifecycle of React is Mounting (an instance of a component being created and inserted into the DOM)
- order of occurance: 
  1. `constructor`
  2. `render`
  3. React Updates
  4. `componentDidMount`
  5. `componentWillUnmount`
- `componentDidMount` - is used if you need to load anything using a network request or initialize the DOM

# React State vs Props

- anything can be passed down from parent to child
-  props are external and controlled by whatever renders the component while state is internal and controlled by the component itself
- react components automatically re-render whenever there is a change in their state or props
- a component state should be able to store any sort of data type, input elements, form, checkbox.

## Things I want to know more about