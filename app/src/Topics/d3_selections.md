<!---
{"next":"Topics/d3_datajoins.md","title":"D3 Selections"}
-->

# Selections

D3 employs a declarative approach, operating on arbitrary sets of nodes called `selections`. If you know another DOM framework like [jQuery](https://jquery.com/), you'll notice similarities in D3's syntax and principles.

For example, if you want to turn the font in all <p> tags blue in JS, the code can get clunky. D3 makes it much simpler, while still allowing you to manipulate individual `selection` nodes as needed.

```javascript
d3.selectAll("p")
	.style("color", "blue");

d3.select("body")
	.style("background-color", "black");
```

In this example, we select elements using the tag name. You can select elements using the:
* Tag name
* Containment
* Attribute values
* Class
* ID

D3 also provides numerous methods for mutating nodes, including:
* Setting attributes or styles
* Registering event listeners
* Adding, removing or sorting nodes
* Changing HTML or text content

Let's walk through an example of how you'd set up to create a data vizualization with D3.

```html
<div id="my_dataviz"></div>
```

This creates a `<div>` where the graph will take place.

```javascript
// Append the svg object to the body of the page
var svg = d3.select("#my_dataviz")
  .append("svg") // you can add dimensions & margins here

//Read the data
d3.csv("https://raw.githubusercontent.com/holtzy/data_to_viz/master/Example_dataset/3_TwoNumOrdered_comma.csv")

// When reading the csv, you need to format variables:
function(d){
  return { date : d3.timeParse("%Y-%m-%d")(d.date), value : d.value }
},

  // Now you're ready to use this dataset!
```

## D3 Code Along 1 - [Selections](https://codepen.io/jkeohan/pen/rZYRye?editors=0010)

