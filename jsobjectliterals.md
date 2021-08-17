# JavaScript Object Literals: The DOM

## Creating an Object
- use literal notation
- object is a series of variables and functions that represent something
- in objects, varables are *properties* of the object
- web browsers implement objects that rep both the window and the document
- JS has several built-in objects:
  - string
  - number
  - math
  - date
- arrays and objects create complex data sheets

## Document Object Model

### Creating DOM Queries
- methods that find elements in the DOM tree are DOM queries
- storing elements in variables = storing the location of the element(s) within the DOM tree in a variable
- `getElementById()` and `querySelector()` can bothe search document and return elements
- to select form a NodeList:
  - The `item()` method
  - Array syntax
- you can loop NodeLists through each node in the collection and apply same statements to each
- Adding or Removing HTML Content
  - `innerHTML` - retrieve and replace content by saving content as a string in a variable, selecting the element whose content you want to replace, set the element's `innerHTML` to the new string; to remove content, set `innerHTML` to an empty string
- DOM Manipulation Methods
  - Approach - refers to a set of DOM methods that allow you to create element and text nodes. To do this, add content one node at a time and store it in a variable then another DOM is used to attatch it to the right place in DOM tree; to remove, use a single method
- Attribute Nodes
  - once you have an element node, you can use other properties and methods on that node to access and change its attributes

[Home](reading-notes.md) 