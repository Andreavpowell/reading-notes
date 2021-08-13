# HTML Links

## Links
- created using the `<a>` (anchor) element
- users can click on anything within the opening and closing tags
- specifiy the page you want to link to by using the `href` attribute
- `<a href="http://ww.site.com">SITE</a>`
  - opening link tag - `<a href="http://ww.site.com">`
  - site the link takes you to - `http://ww.site.com`
  - the text the user clicks - `SITE`
  - closing tag - `</a>`
- the text between the anchor tags is *link text*
- clear link text will give a more positive impression and may encourage them to visit for longer, also helps using screen reader software
- instead of "places to eat" use "brunch in Huntington Beach"
- when linking to places in the same site, use a relative url
- if using relative url to page in same folder, use:
  - `index.html`
  - `about-us.html`
  - `contact.html`
- if in different folders, use:
  - `movies/dvd/reviews.html`
- email link:
  - `<a href="mailto:andrea@example.com">Email Andrea</a>`
- new window link:
  - `<a href="http://ww.site.com" target="_blank">SITE</a>`
- link id on same page:
  - `<a href="#about_us">About Us</a>`
  - `<h3 id="about_us">About Us</h3>`

# CSS Layout

## Building Blocks
- CSS treats HTML elements as a box
- boxes are either:
  - block-level elements
  - inline elements
- block-level
  - start on new line
  - `<h1> <p> <ul> <li>`
- inline
  - flow in between surrounding text
  - `<img> <b> <i>`

## Containing Elements
- if a block-level element is inside another, the outer box is the *containing* or *parent* element
- even if more than one element is inside, the containing element is always the direct parent
- can group together similar elements that control the same part of code using `<div>`
- the `<div>` element that contains the other similar elements is the *containing* element

## Postition of elements
- normal flow
  - every block-level is on a new line
  - default behavior
- relative positioning
  - moves element from the position it defaults to 
  - does not affect position of surrounding elements
- absolute positioning
  - positions element in relation to its containing element
  - taken out of normal flow, doesn't affect surrounding elements, and moves as users scroll up and down
- fixed positioning
  - form of absolute
  - positions element in relation to the browser window instead of the containing element
  - doesn't effect surrounding element positioning
  - doesn't move when user scrolls
- floating elements
  - allows you to take element out of normal flow and position it far left or right of a containing box
  - becomes a block-level element around which other content cna flow
- when you move element from normal flow, boxes overlap. `z-index` allows you to determine which box is on top

## Screen Size
- your design must fit all different screen sizes

## Screen Resolution
- resolution refers to the number of dots a screen shows per inch
- higher resolution = smaller text

## Page Sizes
- most devs try to create pages around 960-1000 pixels wide

## Fixed Width Layouts
- do not change size and user increases or decreases their window
- tend to be in pixels
- advantages:
  - helps control element size and position
  - more control over appearance
  - control length of lines of text regardless of user window size
  - img size will always stay rel to rest of page
- disadvantages:
  - can end up with gaps around page edge
  - if user screen is higher res, page can look smaller and harder to read
  - works best on devices that have site or res similar to desktop or laptop
  - if user increases font size, text might not fit in allotted spaces
  - often take up more vertical space than a liquid layout

## Liquid Layouts
- stretch and contract as user increases or decreases browser size
- tend to use percentages
- advantages:
  - pages expand to fill window
  - if user has small window, page can contract to fit without user having to scroll sideways
  - tolerant of users setting their own font sizes
- disadvantages:
  - if you don't control width of sections of the paeg, design can look different than intended
  - unexpected gaps
  - items can get squished
  - if user has wide window, text can become very long and harder to read
  - if a fixed width item (img) is in a box that is too small (because user made window smaller), img can overflow txt  

  *grids create pro and flexible designs*
  
# JS Functions; Methods and Objects

## Declaring a function
- create a function
  - give it a name
  - write statements to achieve a task between curly braces
  - *function declaration*
- `function sayHello() {  
  document.write('Hello!');  
}`
  - function keyword - `function`
  - function name (identifier) - `sayHello()`
  - code block (statements) - `{  
    document.write('Hello!') 
  }`


## Calling a Function
- to run the code, use the function name followed by parenthesis
  - `sayHello();`
- this code *calls a function*
- call as many times as you want

## Declaring Functions That Need Info
- when you do this, use *parameters*
- inside the funciton, parameters act like variables
- parameters are the parenthesis after the name
- `function getArea(width, height) { 
  return width * height;  
}`
  - each time you call this function, the values could be different
  - demonstrates code can perform task without knowing exact details in advance as long as it has rules

## Calling Functions That Need Info
- you specify the values it should use in the parenthesis that follow the name
- called *arguments*
- can be values or variables
- arguments as values
  - `getArea(3, 5);`
  - 3 will be used for width, 5 will be used for height
- arguments as variables
  - `wallWidth = 3;  
     wallHeight = 5;  
     getArea(wallWidth, wallHeight);`
  - do not have to specify when calling, can use variables instead
- parameters vs arguments
  - parameters - words act like variables
  - arguments - numbers act like values

## Getting Single Value out of Function
- some functions return info to the code that called them
- `function calculateArea(width, height) {
  var area = width * height;
  return area;
}
  var wallOne = calculateArea(3, 5);
  var wallTwo = calculateArea(8, 5);`
  - `calculateArea` - returns area to code that called it
  - variable called area is created and holds calculated area of the box
  - `return` is used to return value to the code that called it

## Getting Multiple Values out of Function
- use array
- `function getSize(width, height, depth) {
  var area = width * height;
  var volume = width * height * depth;
  var size = [area, volume];
  return sizes;
}
  var areaOne = getSize(3, 2, 3)[0];
  var wallTwo = getSize(3, 2, 3)[1];`
  - area and volume are placed in an array called sizes
  - array is then returned to the code that called `getSize()`
  - area is the first value in the array
  - volumeOne variable holds volume of a box that is 3 x 2 x 3
  - volume is the second value in the array

# 6 Reasons for Pair Programming

## Greater Efficiency
- easier to catch mistakes with 2 people
- produces higher quality code
- 2 people researching

## Engaged Collaboration
- stops you from procrastinating
- rely more on each other
- boosts confidence

## Learning from Fellow Students
- exposes you to different techniques
- may have different skill sets

## Social Skills
- improves social skills
- work together
- shows employers you work well with others

## Job Interview Readiness
- common interviews have you pairing with an employee

## Work Environment Readiness
- many companies expect to train fresh hires from cs-degree programs
- CF teaches you how to be ready with pairing  

[Home](reading-notes.md)