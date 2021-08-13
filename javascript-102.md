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
* Compiled languages - transformed (compiled) into another form before they are run. (C/C++ are compiled into machine code that is then run by the computer. The program is executed from a binary format that was generated from the original program source code)

### Server-Side VS Client-Side Code
* Client-Side code is code that is run on the *computer* itself when a web page is viewed. It's downloaded, then run and displayed by the browser.
* Server-Side code is run on the *server*, then it's results are downloaded and displayed in the browser. (PHP, Python, Ruby, ASP.NET, JavaScript)

### Dynamic VS Static Code
* Dynamic describes client-side JS and server-side languages. It refers to being able to update the display of a web page/app to show different things in different circumstances, generating new content as required.
* Static is a web page with no dynamically updating content. It just shows the same content all the time. 

# How to add
### JavaScript
1. Make a local copy of your file (ex. apply-javascript.html) and save it in a sensible directory.
2. Open file in browser and text editor. HTML creates a simple web page containing a clickable button.
3. Go to your editor and add the following in your `head` just before your closing `</head>` tag:
`<script>` *enter*  `// JavaScript goes here` *enter*
`</script>`
4. Add JS code inside `<script>` element under the `// JavaScript goes here` line. 
5. Save your file and refresh browser
> Broke something? Go through the steps again. Save local copy with `.html` extension? Did you add `<script>` element before `<head>`? JS is case sensitive. Be very exact.

### External JavaScript
1. Create new file in the same  directory as your HTML file. Call it `script.js`. Must be JavaScript extension.
2. Replace current `<script>` element with: `<script src='script.js" defer></script>`
3. Insert your JS code
4. Save file and refresh browser

### Inline JavaScript Handlers
* JS that lives inside your HTML    
* DON'T DO THIS

# Script Loading Strategies
* HTML is always loaded in the  order that it appears causing JavaScript to run before your HTML elements. An Event Listener listens for the browser's `DOMContentLoaded` event which signifies that the HTML body is loaded and parsed. The JS in this block will not run until after that event is fired so the error is avoided.
* The `defer` attribute tells the browser to continue downloading the HTML content once the `<script>` tag has been reached. With this, both the script and HTML will load simultaneously and successfully.
* `async` and `defer` can both bypass the problem of blocking script. Scripts loaded with an `async`  attribute will download script without blocking the page while the script is being fetched. When complete, the script will execute which blocks the page from rendering. No guarantee they will run in order. Best to use `async` when the scripts run independently from one another and depend on no other script.
* Script with `defer` will load in order and won't run until all page content is loaded which is useful is your scripts depend on the DOM being in place.
![script loading methods](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/What_is_JavaScript/async-defer.jpg)
Img from the [HTML spec](https://html.spec.whatwg.org/images/asyncdefer.svg)
* `async` should be used when you cave a bunch of background scripts to load in and you just want to get them in as soon as possible.
* `async` and `defer` are both used to instruct the browser to download the scripts in a separate thread while the rest of the page loads.
 
# Comments
* Single line comment 
  * `// I am a comment`
* Multi-line comment
  * `/*` *enter* `I am also` *enter* `a comment` *enter* `*/`

# JavaScript Variables
* The three ways to declare a JavaScript variable:
  * `var`
  * `let`
  * `const`
* Conatiners for storing data
* Works similar to algebra

# JavaScript Identifiers
* All variables must be identified iwth unique names called *identifiers*.
* Can be short names like x and y or more descriptive like sum, age, and totalVolume.
* The rules of using names for variables:
  * can contain letters, digits, underscores, and dollar signs
  * must begin with a letter
  * can begin with $ and _
  * case sensitive
  * reserved words (like JS keywords) cannot be used as names

### Assignment Operator
* `=` is an assesment, not an "equal to" order
* `x = x + 5` does not make sense in algebra, but makes sense in JS as it assigns the value of x + 5 to x
* `==` is "equal to" in JS

### JavaScript Data Types
* JS variables can hold numbers and text values
* Text values are called text strings
* Strings are written inside double or single quotes. Numbers are written without quotes.
* If theres a number in quotes, it will be treated as a text string.

### Declaring JavaScript Variables
* Creating a variable (`var`) in JS is called "declaring" a variable. Without an assigned value, the `var` will be considered `undifined`.
* Assign value by using `=`. `carName = "Volvo";`
* Can also assign a value to the variable when you declare is `var carName = "Volvo";`.
* Then we output the value inside an HTML paragraph with `id='demo`.
* Separate variables with a comma.
* Can span multiple lines.

### Re-Declaring JavaScript Values
* If you re-declare a JS variable, it will not lose it's value.
* Ex: the variable for `carName` will still have a value of "Volvo" after the execution of `var carName;` again even if you don't add a value at the end.

# JavaScript Arithmetic
* Arithmetic with JavaScript variables uses operators like `=` and `+`.
*  You can add strings, but they will not be concatenated.
* If you put a number in quotes, the rest of the numbers will be treated as strings and concatenated.
* JS treats `$` and `_` as a letter, but `$` is not very commonly used.


[Home](reading-notes.md)
