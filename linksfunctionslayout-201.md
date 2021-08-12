#  HTML Links, JS Functions, and Intro to CSS Layout

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
  
##