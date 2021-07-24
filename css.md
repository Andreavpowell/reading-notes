# CSS
Cascading Style Sheets lets you create the "pretty side" of your site within markup languages. CSS is rule-based.

> Browsers are sometimes called _user agents_ which means a program represents a person in a computer system.

### CSS Syntax
* Rules open with a *selector*. This selects the html element to style.
* Then there are curly brackets ({}). Inside these will be declarations which take form of property and value pairs. Each pair specifies a property of the element, then  a value we would like to give the property.
* Before the colon (;), is a property. After the colon, the value. 
* https://developer.mozilla.org/en-US/docs/Web/CSS/Reference

### CSS Modules
* CSS is broken into modules. Find moduels in the link above

### CSS Specifications
* All web standard technologies are defined in documents called *specifications* or *specs* which are published by standards organizations and determine how they behave.
* CSS is developed by a group within the W3C called the CSS Working Group.

> Always check browser compatibility on specs


# How to add CSS
* Three ways of inserting CSS:
  * External CSS
  * Internal CSS
  * Inline CSS

### External CSS
* Can change entire look of site by only altering one file
* Each HTML page must include a reference to the external style sheet file inside the `link` element inside of the `head` element. `<link rel="stylesheet" href="mystyle.css">`
* Can be written in any text editor
* Must be saved with a .css extension (this cannot contain any HTML tags)

### Internal CSS
* Defined within the `style` element inside the `head`

### Inline CSS
* May be used to apply style to a single element
* Just add the style attribute to the relevant element
* Loses many of the advantages of a style sheet
* Use this sparingly

### Multiple Style Sheets
* If properties have been defined for the same element in different style sheets, the value from the last read style sheet will be applied.

### Cascading Order
* All styles will "cascade" into a new "virtual" style sheet by these rules:
  * Inline style (inside element)
  * External and internal style sheets (in `head`)
  * Browser default

# CSS Color Properties

### CSS Syntax
* `color: red|initial|inheret;`

### Property Values
* `color` - specifies the text color
* `initial` - sets this property to its default value
* `inherit` - inherits this property from it's parent element

### Examples
* HEX - `body {color: #92a8d1;`
* RGB - `body {color: rgb(201, 76, 76);}   `
* RGBA - `body {color: rgba(201, 76, 76, 0.6);}`
* HSL - `body {color: hsl(89, 43%, 51%);}`
* HSLA - `body {color: hsla(89, 43%, 51%, 0.6);}`






