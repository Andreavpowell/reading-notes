# React Docs - Forms

- What is a ‘Controlled Component’?
  - an input form element whose value is controlled by React
- Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
  - update as the user goes so that it updates the value of the state *and* the form.
- How do we target what the user is entering if we have an event handler on an input field?
  - add a name attribute and let the handler function choose what to do based on the value of `event.target.name`

# The Conditional (Ternary) Operator Explained

- Why would we use a ternary operator?
  - makes it shorter and easier in some cases
- Write a ternary statement:  
  - `x === y ? true : false`

## Things I want to know more about