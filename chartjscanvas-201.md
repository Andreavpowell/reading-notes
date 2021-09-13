# Chart.js and Canvas 

## Chart.js

### Drawing a line chart

- create a canvas element in your HTML so Chart.js can draw your chart
  - add this to body elem - `<canvas id="buyers" width="600" height="400"></canvas>`
- write a script that will retrieve the context of the canvas
  - add this to foot of your body elem - `<script>  var buyers = document.getElementById("buyers").getContext("2d"); new Chart(buyers).Line(buyerData); </script>`
- inside same script tags, you create your data
- in this instance, it's an object that contains labels for the base of our chart and datasets to describe the values on the chart
  - add this immediately above the line that begins `var buyers=` - `var buyerData = { labels : ["Jan", "Feb", "Mar", "Apr", "May", "Jun"], datasets : [ { fillColor : "rgba(123, 123, 123, 0.1)", strokeColor : "rgba(123, 123, 123, 0.1)", pointColor : "rgba(123, 123, 123, 0.1)", pointStrokeColor : "rgba(123, 123, 123, 0.1)", data : [123, 123, 123, 123, 123, 123] } ] }`

### Drawing a pie chart

- same canvas element rules
  - `<canvas id="countries" width="600" height="400"></canvas>`
- same context and instantiation
  - `<script>  var countries = document.getElementById("countries").getContext("2d"); new Chart(countries).Line(pieData, pieOptions); </script>`
- supply some options to the chart
- creating the data is a little different here because the pie chart is simpler (just supply a value and a color for each section)
  - `var pieData = [ { value: 20, color: "12345" }, { value: 40, color: "12345" } { value: 10, color: "12345" }, { value: 30, color: "12345" } ];`
- now immediately after the pieData we'll add our options
  - `var pieOptions = { segmentShowStroke : false, animateScale : true }`
  - these options remove the stroke from the segments and animate the scale of the pie so that it zooms out from nothing

### Drawing a bar chart

- same canvas rules
  - `<canvas id="income" width="600" height="400"></canvas>`
- retrieve the element and create graph
  - `var income = document.getElementById("income").getContext("2d"); new Chart(income).Bar(barData);`
- add the data
  - `var barData = { labels : ["Jan", "Feb", "Mar", "Apr", "May", "Jun"], datasets : [ { fillColor : "#48A497", strokeColor : "#48A497", data : [123, 123, 123, 123, 123, 123] }, { fillColor : "#48A497", strokeColor : "#48A497", data : [123, 123, 123, 123, 123, 123] } ] }`

## Basic Usage of Canvas

- the element
  - `<canvas id="tutorial" width="150" height="150"></canvas>`
  - `<canvas id="stockGraph" width="150" height="150">` `current stock price: $3.15 + 0.15 </canvas> <canvas id="clock" width="150" height="150">`
  `<img src="images/clock.png" width="150" height="150" alt=""/> </canvas>`
  - use `getContext()` to render context
  - `var canvas = document.getElementById('tutorial'); var ctx = canvas.getContext('2d');`
  - check for support
  - `var canvas = document.getElementById('tutorial');` `if (canvas.getContext) { var ctx = canvas.getContext('2d');`
  `// drawing code here } else {`
  `// canvas-unsupported code here }`
  
### Drawing Shapes

- rectangles:
  - `fillRect(x, y, width, height)` - draws a filled rectangle
  - `strokeRect(x, y, width, height)` - draws a rectangular outline
  - `clearRect(x, y, width, height)` - clears the specified rectangular area, making it fully transparent
- paths:
  - list of points connected by segments of lines that can be of different shapes, width, and color
  1. create path
  2. use drawing commands to draw into path
  3. once path is created, stroke or fill path to render it
  - `beginPath()` - creates a new path, future drawing commands are directed into the path and used to build the path up
  - Path methods - set different paths for objects.
  - `closePath()` - adds a straight line to the path, going to the start of the current sub-path
  - `stroke()` - draws the shape by stroking its outline
  - `fill()` - draws a solid shape by filling the path's content area
- triangles:
  - `function draw() {`
  `var canvas = document.getElementById('canvas');`
  `if (canvas.getContext) {`
    `var ctx = canvas.getContext('2d');`
   ` ctx.beginPath();`
   ` ctx.moveTo(75, 50);`
    `ctx.lineTo(100, 75);`
    `ctx.lineTo(100, 25);`
    `ctx.fill(); } }`
- moving the pen:
  - like lifting a pen from one spot on a page to another
  - `moveTo(x, y)` - moves the pen to the coordinates specified by x and y
  - when the canvas is initialized or `beginPath()` is called, you typically will want to use the `moveTo()` function to place the starting point somewhere else
  - could also use `moveTo()` to draw unconnected paths
- lines:
  - `lineTo(x, y)` - draws a line from the current drawing position to the position specified by x and y
- arcs:
  - `arc(x, y, radius, startAngle, endAngle, counterclockwise)` - draws an arc which is centered at `(x, y)` position with radius r starting at `startAngle` and ending at `endAngle ` going in the given direction indicated by `counterclockwise` (defaulting to clockwise)
  - `arcTo(x1, y1, x2, y2, radius)` - draws an arc with the given control points and radius, connected to the previous point by a straight line
- making combinations
  - `fillStyle` property on the drawing context, and the use of a utility function (in this case `roundedRect()`)
- path2D objects:
  - `Path2D()` - this constructor returns a newly instantiated `Path2D` object, optionally with another path as an argument (creates a copy), or optionally with a string consisting of SVG path data
- SVG paths:
  - use this to initialize paths on canvas

### Applying Styles and Colors

- colors:
  - `fillStyle = color` - sets the style used when filling shapes
  - `strokeStyle = color` - sets the style for shapes' outlines
  - `globalAlpha = transparencyValue` - applies the specified transparency value to all future shapes drawn on the canvas. The value must be between 0.0 (fully transparent) to 1.0 (fully opaque). This value is 1.0 (fully opaque) by default
- line styles:
  - `lineWidth = value` - sets the width of lines drawn in the future
  - `lineCap = type` - sets the appearance of the ends of lines
  - `lineJoin = type` - sets the appearance of the "corners" where lines meet
  - `miterLimit = value` - establishes a limit on the miter when two lines join at a sharp angle, to let you control how thick the junction becomes
  - `getLineDash()` - returns the current line dash pattern array containing an even number of non-negative numbers
  - `setLineDash(segments)` - sets the current line dash pattern
  - `lineDashOffset = value` - specifies where to start a dash array on a line
- gradients:
  - `createLinearGradient(x1, y1, x2, y2)` - creates a linear gradient object with a starting point of `(x1, y1)` and an end point of `(x2, y2)`
  - `createRadialGradient(x1, y1, r1, x2, y2, r2)` - creates a radial gradient. The parameters represent two circles, one with its center at `(x1, y1)` and a radius of r1, and the other with its center at `(x2, y2)` with a radius of `r2`
  - `createConicGradient(angle, x, y)` - creates a conic gradient object with a starting angle of angle in radians, at the position `(x, y)`
- patterns: 
  - `createPattern(image, type)` - creates and returns a new canvas pattern object. image is a CanvasImageSource (that is, an HTMLImageElement, another canvas, a <video> element, or the like. type is a string indicating how to use the image
  - `repeat` - tiles the image in both vertical and horizontal directions
  - `repeat-x` - tiles the image horizontally but not vertically
  - `repeat-y` - tiles the image vertically but not horizontally
  - `no-repeat` doesn't tile the image. It's used only once
- canvas fill rules:
  - `nonzero` - the non-zero winding rule, which is the default rule.
  - `evenodd` - the even-odd winding rule.
- drawing text:
  - `fillText(text, x, y [, maxWidth])` - fills a given text at the given `(x,y)` position. Optionally with a maximum width to draw
  - `strokeText(text, x, y [, maxWidth])` - strokes a given text at the given `(x,y) ` position. Optionally with a maximum width to draw
- styling text:
  - `font = value` - the current text style being used when drawing text. This string uses the same syntax as the CSS font property. The default font is 10px sans-serif.
  - `textAlign = value` - Text alignment setting. Possible values: start, end, left, right or center. The default value is start.
  - `textBaseline = value` - Baseline alignment setting. Possible values: top, hanging, middle, alphabetic, ideographic, bottom. The default value is alphabetic.
  - `direction = value` - Directionality. Possible values: ltr, rtl, inherit. The default value is inherit.

[Home](reading-notes)