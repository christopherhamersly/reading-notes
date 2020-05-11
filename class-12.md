# Docs for the HTML < canvas > Element & Chart.js
  * Charts are far better for displaying data visually than tables and have the added benefit that no one is ever going to press-gang them into use as a layout tool. 
  * Chart.js - is a great place to get started with charts.  It is a javascript plugin that uses HTML's canvas element to draw the graph onto the page.  
  * Download chart.js, copy the chart.min.js out of the unzipped folder. 
  * To draw a line chart, the first thing we need to do is create a canvas element in our HTML in which Chart.js can draw our chart. So add this to the body of our HTML page ( <canvas id="buyers" width="600" height="400"></canvas> )
  * Next, we need to write a script that will retrieve the context of the canvas, so add this to the foot of your body element: <script> var buyers = document.getElementById('buyers').getContext('2d');
    new Chart(buyers).Line(buyerData) </script>
    * Inside the same script tags we need to create our data, in this instance it’s an object that contains labels for the base of our chart and datasets to describe the values on the chart. Add this immediately above the line that begins ‘var buyers=’: var buyerData = { labels : ["January","February","March","April","May","June"], 
    datasets : [
		  {
			fillColor : "rgba(172,194,132,0.4)",
			strokeColor : "#ACC26D",
			pointColor : "#fff",
			pointStrokeColor : "#9DB86D",
			data : [203,156,99,251,305,247]
		  }
    * Drawing a pie chart
     Our line chart is complete, so let’s move on to our pie chart. First, we need the canvas element: <canvas id="countries" width="600" height="400"></canvas>
      Next, we need to get the context and to instantiate the chart: var countries= document.getElementById("countries").getContext("2d"); new Chart(countries).Pie(pieData, pieOptions); You’ll notice that this time, we are going to supply some options to the chart.
      Next we need to create the data. This data is a little different to the line chart because the pie chart is simpler, we just need to supply a value and a color for each section: var pieData = [
	    { 	value: 20,
		  color:"#878BB6"
	    },
	    {
		    value : 40,
		    color : "#4ACAB4"
	    },
	    {
	  	value : 10,
		  color : "#FF8153"
	    },
	  {
		value : 30,
		color : "#FFEA88"
	    }
      ];

# Basics usage of canvas
  * At first sight a < canvas > looks like the < img > element, with the only clear difference being that it doesn't have the src and alt attributes.  The id attribute isn't specific to the  < canvas > element but it is one of the global HTML attributes, which can be applied to any HTML element.  It can be styled like and normal page. It easy to define some fallback content for older browsers.  Providing fallback content is very straightforward: just insert the alternate content inside the < canvas > element. 
    * The < canvas > element creates a fixed-size drawing surface that exposes one or more rendering contexts, which are used to create and manipulate the content shown. In this tutorial, we focus on the 2D rendering context. Other contexts may provide different types of rendering; for example, WebGL uses a 3D context based on OpenGL ES.
    * The canvas is initially blank. To display something, a script first needs to access the rendering context and draw on it. The < canvas > element has a method called getContext(), used to obtain the rendering context and its drawing functions. getContext() takes one parameter, the type of context. For 2D graphics, such as those covered by this tutorial, you specify "2d" to get a CanvasRenderingContext2D.

# Drawing shapes with Canvas
  * fillRect(x, y, width, height) - Draws a filled rectangle.
  * strokeRect(x, y, width, height) - Draws a rectangular outline.
  * clearRect(x, y, width, height) - Clears the specified rectangular area, making it fully transparent.
  * beginPath() - Creates a new path. Once created, future drawing commands are directed into the path and used to build the path up.
  * Path methods - Methods to set different paths for objects.
  * closePath() - Adds a straight line to the path, going to the start of the current sub-path.
  * stroke() -Draws the shape by stroking its outline.fill()Draws a solid shape by filling the path's content area.
  * The first step to create a path is to call the beginPath(). Internally, paths are stored as a list of sub-paths (lines, arcs, etc) which together form a shape. Every time this method is called, the list is reset and we can start drawing new shapes.
  * arc(x, y, radius, startAngle, endAngle, anticlockwise) - Draws an arc which is centered at (x, y) position with radius r starting at startAngle and ending at endAngle going in the given direction indicated by anticlockwise (defaulting to clockwise).
  * arcTo(x1, y1, x2, y2, radius) - Draws an arc with the given control points and radius, connected to the previous point by a straight line.
  * quadraticCurveTo(cp1x, cp1y, x, y) Draws a quadratic Bézier curve from the current pen position to the end point specified by x and y, using the control point specified by cp1x and cp1y.
  * bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x, y) Draws a cubic Bézier curve from the current pen position to the end point specified by x and y, using the control points specified by (cp1x, cp1y) and (cp2x, cp2y).

  * Path2D() -The Path2D() constructor returns a newly instantiated Path2D object, optionally with another path as an argument (creates a copy), or optionally with a string consisting of SVG path data.
    * new Path2D();     // empty path object
    * new Path2D(path); // copy from another Path2D object
    * new Path2D(d);    // path from SVG path data
    * All path methods like moveTo, rect, arc or quadraticCurveTo, etc., which we got to know above, are available on Path2D objects.

    * The Path2D API also adds a way to combine paths using the addPath method. This can be useful when you want to build objects from several components, for example.

    * Path2D.addPath(path [, transform])
    * Adds a path to the current path with an optional transformation matrix.
	
# Colors 
  * fillStyle = color - Sets the style used when filling shapes.
  * strokeStyle = color - Sets the style for shapes' outlines.
  * Transparency - In addition to drawing opaque shapes to the canvas, we can also draw semi-transparent (or translucent) shapes. This is done by either setting the globalAlpha property or by assigning a semi-transparent color to the stroke and/or fill style.
  * globalAlpha = transparencyValue -Applies the specified transparency value to all future shapes drawn on the canvas. The value must be between 0.0 (fully transparent) to 1.0 (fully opaque). This value is 1.0 (fully opaque) by default.
  * The globalAlpha property can be useful if you want to draw a lot of shapes on the canvas with similar transparency, but otherwise it's generally more useful to set the transparency on individual shapes when setting their colors.
  * Because the strokeStyle and fillStyle properties accept CSS rgba color values, we can use the following notation to assign a transparent color to them.
  * lineWidth = value - Sets the width of lines drawn in the future.
  * lineCap = type - Sets the appearance of the ends of lines.
  * lineJoin = type - Sets the appearance of the "corners" where lines meet.
  * miterLimit = value - Establishes a limit on the miter when two lines join at a sharp angle, to let you control how thick the junction becomes.
  * getLineDash() - Returns the current line dash pattern array containing an even number of non-negative numbers.
  * setLineDash(segments) - Sets the current line dash pattern.
  * lineDashOffset = value Specifies where to start a dash array on a line.
  The lineCap property determines how the end points of every line are drawn. There are three possible values for this property and those are: butt, round and square. By default this property is set to butt.
  * butt -The ends of lines are squared off at the endpoints.
  * round - The ends of lines are rounded.
  * square - The ends of lines are squared off by adding a box with an equal width and half the height of the line's thickness.

  # Drawing Text
    * The canvas rendering context provides two methods to render text:
    * fillText(text, x, y [, maxWidth]) - Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.
    * strokeText(text, x, y [, maxWidth]) -Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.
    * Styling text - In the examples above we are already making use of the font property to make the text a bit larger than the default size. There are some more properties which let you adjust the way the text gets displayed on the canvas:
    * font = value - The current text style being used when drawing text. This string uses the same syntax as the CSS font property. The default font is 10px sans-serif.
    * textAlign = value - Text alignment setting. Possible values: start, end, left, right or center. The default value is start.
    * textBaseline = value - Baseline alignment setting. Possible values: top, hanging, middle, alphabetic, ideographic, bottom. The default value is alphabetic.
    * direction = value - Directionality. Possible values: ltr, rtl, inherit. The default value is inherit