# HTML and JavaScript 

## HTML

### Elements for Structure
- each element has opening and closing tags
- `<html>` - indicates anything inside is HTML code
- `<body>` - indicates anything inside is to be shown in the main browser window
- `<h1>` - main heading
- `h2>` - sub-heading
- `<p>` - intro to rest of page (contents of paragraph)

### Closer look at Tags
- `<` left-angle bracket
- `>` right-angle bracket
- between the two is a character
- characters indicate tag's purpose
- `/` forward slash 
- forward slash indicated the closing tag

### Attributes
- provide additional info about the contents of the element
- appear in opening tag
- made of *name* and *value*
- name indicates the extra info in lowercase
- value indicates the setting for the attribute in double quotes
- `<p lang="en-us">Paragraph in English</p>`
- majority of atttributes can only be used with certain elements
- `lang` can be in any element

## Extra Markup

### Escape Characters
- if you want characters to appear in  your page but are normally used for markup, you must use an escape character (entity references)
- always check page to make sure it worked
- some fonts don't support all characters
- `&lt` or `&#60` - < 
- `&gt` or `&amp` - >
- `&amp` or `&#38` - &
- `&copy` or `&#169` - copyright
- `&quot` and `&#34` - "
- `&cent` and `&#162` - cent sign
- `&pound` and `&#163` - pound sign
- `&yen` and `&#165` - yen
- `&euro` and `&#8364` - euro
- `&reg` and `&#174` - registered trademark
- `&trade` and `&#8482` - trademark
- `&lsquo` and `&#8216` - left single quote
- `&rsquo` and `&#8217` - right single quote
- `&ldquo` and `&#8220` - left double quotes
- `&rdquo` and `&#8221` - right double quotes
- `&times` and `&#215` - multiplication sign
- `&divide` and `&#247` - division sign

### Markup Examples
- `DOCTYPES` - tells browser which version of HTML
- `<!--` and `-->` - add comments
- `id` and `class` - attributes add identity to particular elements
- `<div>` and `<span>` - group block-level and inline elements together
- `<iframes>` - cut windows into your web page through which other pages can be displayed
- `<meta>` - supplies info about your page

## HTML5 Layout
- elements indicate the purpose of different parts of a page and help describe the structure
- new elements for clean code 
- older browsers dont understand some HTML5 elements (need to be told which elements are block-level)
- to make it work in Internet Explorer 8 and older, extra JS is needed (available free from Google)\

## Process & Design

- view personal notes from 102 for site map and wireframe
- understand target audience, why they would visit, what info they want on your site, and when they may return
- site map is for planning structure
- wireframes let you organize info
- design is communication 
- use size, color, and style
- use grouping and similarity to simplify info

## JavaScript ABCs

### A
- what is a script and how to create one?
  - series of instrucitons for computer to reach a goal
  - recipies, handbooks, manuals
  - state goal, then list the tasks to achieve it
  - define the goal, design the script, then code each step
  - design using flowcharts or steps

### B
- how do computers fit in with the world?
  - recieves page as HTML, creates a model and stores it, then uses a rendering engiine to display the page
  - major browsers use a JS interpreter
  - uses objects that can contain: properties; methods; events.
  - each element creates a node

### C
- how to write a script?
  - `.html` files - content layer
  - `.css` files - presentation layer
  - `.js` files - behavior layer
  - `document.write('Good Afternoon!');`
  - `document` - represents entire page
  - `.` - member operator
  - `'Good Afternoon!'` - parameters
  - `write('Good Afternoon!')` - write method of the document object
  - use `<script>` elements
  - best to keep js in it's own file with the `.js` extension
  - `<link>` is used for CSS

[Home](reading-notes)

