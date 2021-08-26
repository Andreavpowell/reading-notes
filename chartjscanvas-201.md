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

- 