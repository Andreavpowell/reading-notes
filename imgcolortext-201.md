# HTML IMGs

## Your IMG Should:
- be relevant
- give info
- give right mood
- instantly recognizable
- fit color palette

## Storing IMGs on Your Site
- store in file titled "images"
- use sub folders on larger sites
- logos and buttons could be in "interface"
- product photos could be in "products"
- news imgs could be in "news"

## Adding IMGs
- `<img>`
- an empty tag
- must contain source and alt attributes
- can contain title
- `<img src="xyz.jpg" alt="display text" title="additional info when hovered over" />`

## Height and Width
- two more attributes `<img>` can use
- height and width in pixels
- `<img src="xyz.jpg" alt="display text" height="450" width="600" />`

## IMG Placement
- before paragraph
  - p starts on new line below img
- inside start of paragraph
  - first row aligns with bottom of img
- in middle of paragraph
  - img placed between the words of the p 
- where you place depends on your code
  - if img is followed by block level element, the block level element will appear on new line below img
  - if img is inside the block level element, any txt or inline element will flow around img  

*Block elements always appear on a new line. Ex: `<h1>` and `<p>`.*  
  
*Inline elements sit within a block level element and do not start new line. Ex: `<b>`, `<em>`, and `<img>`.*  
  
## Rules for creating IMGs
- Save in right format
  - will mainly use .jpeg, .gif, or .png
- Save at right size
- Use correct resolution
  - resolution is dots per inch

## Tools to Save and Edit IMGs
- Adobe Photoshop (Photoshop Elements is cheaper)
- Pixelmator
- PaintShop Pro

## JPEG
- photos w lots of colors
- even snow has lots of colors

## GIF or PNG
- photos w less colors or large areas of same color

## IMG Dimensions
- img 600px wide; 300px tall you can reduce img by 50%
  - result: quicker to download
- img 100px wide; 50px tall don't increase size
  - result: blurry or blocky
- img 300px sq you can remove parts of it
  - result: may lose info in img

## IMG Resolution
- resolution = number of squares within 1"x1" sq
- JPGs, GIFs, PNGS = bitmap
  - made of lots of pizels
- most desktop computers display imgs at a res of 72ppi

## Vector IMGs
- not bitmap
- resolution-dependent
- commonly created in programs like Adobe
- like line drawings (logo, illustration, diagram)
- created by placing points on a grid and drawing lines between those points
- can be color
- can increase dimensions without effecting quality

## Animated GIFS
- show several frames in sequence 
- programs like Adobe Photoshop
- each extra frame increases file size, taking longer to download
- mostly only suitable for simple illustrations

## Transparency
- "see-through"
- if transparent part has straight edges and is 100% transparent (not semi-opaque), save as GIF with transparency option selected
- if transparent part has diagonal or rounded edges or if you want semi-opaque or drop shadow, save as PNG (not fully supported in older browsers; can use JS to get around this)

## Examining and Downloading on Web
- checking size
  - right click on img and make selection from pop-up (Mac, hold cntrl and click)
  - to save img, right click > open in new tab > save image as
  
## Figure and Figure Caption
- `<figure>` - contains image(s) and their caption(s) so the two tags are associated with each other, if more than one img both must have same caption for figure tag to work
- `<figcaption>` - allows web page authors to add captions  
  
*Older browsers do not understand new HTML5 elements*

# CSS Color

## Foreground Color
- RGB values 
  - how much red, green, and blue. 
  - rgb(100,100,90)
- HEX codes 
  - 6 digit codes representing red, green, and blue preceeded by a #.
  - Ex: #ee3e80
- color names
  - 147 predefined
- HSLA (later in notes)
- `color: xyz;`

## Background Color
- specify background color same as foreground
- `background-color: xyz;`

## Understanding Color
- every color on screen is made of red, green, and blue
- hue
  - near to the colloquial idea of color
- saturation
  - amount of grey in a color
- brightness (value)
  - how much black in a color

## CSS3: HSL
- hue is represented as a color circle, may sometimes be a slider 0-360
- saturation is 0%-100%, the higher the number the more grey
- lightness (lumosity)
  - amount of white or black, 0%-100%, higher is whiter

*Ensure enough contrast between text and background*

# Text

## Terminology
- serif
  - these fonts have extra details on ends of main strokes
  - the details are called "serifs"
- sans-serif
  - these fonts have straight ends
- monospace
  - each letter is the same width
- ascender
  - above the cap height
- cap height
  - top of flat letters
- x-height
  - height of letter x
- baseline
  - line letter sit on
- descender
  - below the base line
- weight
  - light, medium, bold, black
- style
  - normal, italic, oblique
- stretch
 - condensed, regular, extended

## Choosing Typeface
- browser will only display if it's installed on user's computer

## Type Scales
- developed by European typographers in the late 16th century
- default font size in browser is 16px

## Units of Type Size

### Twelve px scale
<pre>
      |  Pixels  |  Percentages  |  EMS  |
      |----------|---------------|-------|
  h1  |   24px   |      200%     | 1.5em |
  h2  |   18px   |      150%     | 1.3em |
  h3  |   14px   |      117%     | 1.17em|
 body |   12px   |       75%     |  100% |
   p  |          |               | 0.75em|  
</pre>
### Sixteen px scale
<pre>
      |  Pixels  |  Percentages  |   EMS   |
      |----------|---------------|---------|
  h1  |   32px   |      200%     |   2em   |
  h2  |   24px   |      150%     |  1.5em  |
  h3  |   18px   |      133%     | 1.125em |
 body |   16px   |      100%     |   100%  |
   p  |          |               |   1em   |  
</pre>

- pixels
  - best way to ensure type appears as you intended
  - relative to the resolution of the screen
  - can use `pt` for point sizes instead of `px` for pixels but only when creating style sheets for printer friendly versions
- percentages
  - users can change default size of text in web browsers
  - if they do that, font will be displayed at the same scale but larger size
- EMS
  - change the size of text relative to size of text in parent element
  - if user changes size in browser, fonts may look smaller or bigger than intended
  - `p` is to help Internet Explorer 6 and 7 display the fonts correctly 

## Text Summary
- must have right license to use different typefaces
- control space between lines of text, individual letters, and words
- can be aligned left, right, center, justified, or indented
- use pseudo-classes to change style of an element when user hovers or clicks or visits a link

# JPEG vs PNG vs GIF

JPEG
- contain natural scene or photograph with variation in color and smooth intensity  

PNG
- needs transparency or images w text and objects with contrast edges  

GIF
- contain animations
