# Object-Oriented Programming and JS Constructor Funcitons

## Domain Modeling
- process of creaing a conceptual model in code for a problem
- model describes various entities, attributes, behaviors, and the constraints that govern the problem domain
- entities that store data in properties and encapsulates behaviors in meethods is commonly referred to as an object-oriented model
- if articulated well, can verify and validate the understanding of a specific problem among various stakeholders
- defines a vocab that can be used in and between tech and business terms
- `new` instantiates (creates) an object
- constructor function initializes properties inside the object using the `this` variable
- object is stored in a variable for future use
- `Math.random()` function generates a random number


## HTML Tables
- `<table>` 
- `<tr>` start of each row
- `<td>` starts a cell (table data)
- `<th>` table heading
- even if no content, still use `<td>` of `<th>` to indicate it's empty
- for long tables, split into a `<thead>`, `<tbody>`, and `<tfoot>`
- rowspan and colspan attributes make cells span more than one row or colomn

## Creating an Object
- `new` and the object constructor create a blank object (`Object()`)
- can then add properties and methods to object using `.` (dot notation)
- each statement that adds should end with a `;`
- create empty object using literal notation `var cat = {}`
- to update value of properties, use dot notaion or square brackets
- dot notaions and square brackets work on objects created using literal or constructor notation
- to delete a property use `delete`
- can also update properties using square brackets and single quotations
- if object doesn't have the property you are trying to update, it will be added to the object
- new value is after assignment operator
- to clear the value, set it to a blank string using `''`

## Creating Many Objects
- use a template
- `this` is used intesd of the object name - indicated property or method belongs to the object *this* function creates
- each statement that creates a new property ends in a `;`
- constructor function name is capitalizes
- create instances of the object using constructor function
- `new` followed by a call to the funciton creates a new object
- arrays are a special object
- the key for each value in array if it's index number
- arrays in objects and objects in arrays
  - combine to create complex data structures
  - arrays can store a series of objects (and remember order)
  - objects can also hold arrays (as values of properties)
- three groups of built-in objects
  - browser object model - creates a model of the browser tab or window
  - document object model - creates a model of current web page
  - global js objects - do not form single model as they are a group of individual objects that relate to different parts of the js lang

## Creating an Instance of the Date Object
- use `Date()` object constructor
- `var today = new Date()`

[Home](reading-notes)
