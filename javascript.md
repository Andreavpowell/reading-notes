# JavaScript
* JS is a lightweight, just-in-time (executes code that compiles *during* exacution of a program instead of before) language with first-class functions (a function can be passed as an argument to other functions, can be returned by another function and can be assigned as a value to a variable).
* Most commonly used for web pages, but also used bu non-browser environment such as Node.js, Apache CouchDB, and Adobe Acrobat.
* JS
  * is prototype-based
  * is multi-paradigm
  * is single-threaded
  * is a dynamic language
  * supports object-oriented styles
  * supports imperative styles
  * supports declarative styles
### JavaScript Standards
* ECMAScript Language Specification (ECMA-262)
* ECMAScript Internationalization API Specification (ECMA-402)

# JS Baiscs
* Creates dynamically updating content, control multimedia, animate images, and pretty much everything else.
* Stores usefufl values inside variables
* Operates on pieces of text (strings)
* Runs code in response to events (like clicking a button) happening on a web page
* APIs (Application Programming Interfaces) are code building blocks to implement programs that would otherwise be impossible to implement

### Broswer APIs
* Built into your browser and able to expose data from the environment or do useful complex things.
* Examples:
  * `DOM (Document Object Model) API `- allows manipulation of HTML and CSS by removing and changing HTML, dynamically applying new styles to your page, etc. (popup window)
  * `Geolocation API` - retrieves geographical info (Google Maps)
  * `Canvas` and `WebGL` - create animated 2D and 3D graphics
* Always consider cross browser testing

### Third Party APIs 
* Not built into browser by default. Have to grab their code and info from somewhere on the Web.
* Examples: 
  * `Twitter API` - displays latest tweets on your page
  * `Google Maps API` - displays custom maps on your page
### Browser Security 
* Browser tabs have their own separate bucket for running code called *execution environments*.
* Code in each tab is run separately so code in one tab cannot effect another.
* If it weren't for this, pirates could easily start writng code to steal info from sites.

### JS Running Order
When a browser detects JavaScript, it runs it in order from top to bottom. Be careful to place functions in the order you want them to occur. This is a very common error.

### Interpreted VS Compiled Code
* Interpreted languages - runs from top to bottom and result is immediately returned
* Compiled languages - transformed (compiled) into another form before they are run 