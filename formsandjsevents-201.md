# Forms and JavaScrips Events

## Forms
- how they work
  1. user fills a form and then presses a button to submit info to the server
  2. name of each control is sent to the server along with the value the user enters/selects
  3. server processes info using a programming lang like PHP, C#, VB.net, or Java (may also store info in database)
  4. server creates new page to send back to the browser based on the info recieved
- forms can have many form controls with each gathering different info
- server needs to know which piece of inputted data corresponds with which form element
- to differentiate, info is sent from browser to server using name/value pairs. `name=value`


## Lists/Tables/Forms
- in addition to css properties that work with contents of all elements, there are many others that are specifically used to control appearance of lists, tables, and forms
- list markers can be given different appearances using the `list-style-type` and `list-style` image properties
- table cells can have different borders and spacing in different browsers, but there are properties you can use to control them and make them more consistent. 
- forms are easier to use if the form controls are vertically aligned in css
- forms benefit from styles that make them feel more interactive

## Events
- html elements nest inside others so if you hover over or cick on a link, you're also hovering or clicking on its parent elements
  - imagine an `<li>` contains a link
  - when you hover or click on it, js can trigger events on the `<a>` element and other elements the `<a>` element sits in
  - event handlers/listeners can be bound to the containing `<li>`, `<ul>`, `<body>`, and `<html>` elems, plus the `document` object, and the `window` object
  - the order in which the events fire is known as event flow and they flow in two directions
- event bubbling
  - event starts at the most specific node and flows outwards to the least specific one
  - this is default 
- event capturing 
  - event starts at least specific node and flows inwards to the most specific one. 
  - not supported in IE 8 and earlier
- event flow only really matters when your code has event handlers on an element *and* one of it's ancestor or descendant elements
- events occur in screen, page, and client
- events are browsers way of indicating something has happened
- binding is the process of stating which event you are waiting to happen and which element you are waiting for that to happen to 
- event occuring on elements can trigger a js function
- can use event delegation to monitor for events that happen on all children of an element
- most commonly used events are W3C DOM events, although there are others int he HTML5 specification as well as browser-specific events

[Home](reading-notes)
