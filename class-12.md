#  Basic usage of canvas

- At first sight a `<canvas>` looks like the `<img>` element, with the only clear difference being that it doesn't have the src and alt attributes.

- The `<canvas>` element has only two attributes, width and height. These are both optional and can also be set using DOM properties.

- When no width and height attributes are specified, the canvas will initially be **300 pixels wide and 150 pixels high**.

- The element can be sized arbitrarily by CSS, but during rendering the image is scaled to fit its layout size: if the CSS sizing doesn't respect the ratio of the initial canvas, it will appear distorted.

- As a consequence of the way fallback is provided, unlike the `<img>` element, the `<canvas>` element requires the closing tag (`</canvas>`). If this tag is not present, the rest of the document would be considered the fallback content and wouldn't be displayed.

- The `<canvas>` element creates a fixed-size drawing surface that exposes one or more rendering contexts, which are used to create and manipulate the content shown.

- The fallback content is displayed in browsers which do not support `<canvas>`. Scripts can also check for support programmatically by simply testing for the presence of the getContext() method.




# Easily create stuning animated charts with chart.js 

- **Chart.js**: a JavaScript plugin that uses HTML5’s canvas element to draw the graph onto the page. It’s a well documented plugin that makes using all kinds of *bar charts*, *line charts*, *pie charts* and more, incredibly easy.

### To draw a line chart: 

  1. Create a canvas element in our HTML in which Chart.js can draw our chart. So we should add this to the body of our HTML page:

    `<canvas id="buyers" width="600" height="400"></canvas>`

  2. Then we need to write a script that will retrieve the context of the canvas, so wecadd this to the foot of our body element:
  
    <script>
       var buyers = document.getElementById('buyers').getContext('2d');
       new Chart(buyers).Line(buyerData);
    </script>

  3. Inside the same script tags we need to create our data, in this instance it’s an object that contains labels ( an array) for the base of our chart and datasets (fillColor, strokeColor, pointColor, pointStrokeColor and data) to describe the values on the chart.
      ```javascript
      var buyerData = {
    	labels : ["January","February","March","April","May","June"],
        	datasets : [
    		{
    			fillColor : "rgba(172,194,132,0.4)",
    			strokeColor : "#ACC26D",
    			pointColor : "#fff",
    			pointStrokeColor : "#9DB86D",
    			data : [203,156,99,251,305,247]
    		}
    	]
    }
```
### Drawing a pie chart

  1. Create the canvas element.
  2. Get the context and to instantiate the chart (supply some options to the chart).
  3. Supply a value and a color for each section.
  4. Then we add our options : 
      var pieOptions = {
    	segmentShowStroke : false,
    	animateScale : true
      }
    
- **These options do two things, first they remove the stroke from the segments, and then they animate the scale of the pie so that it zooms out from nothing**.

### Drawing a bar chart

   1. First we add the canvas element.
   2. Next, we retrieve the element and create the graph.
   3. And finally, we add in the bar chart’s data.












