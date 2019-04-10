<!---
{"next":"Topics/d3_selections.md","title":"D3 Libraries & Elements"}
-->

# D3 Libraries & Elements

## Importing D3 Libraries

There are several ways to access D3. 

#### npm
* Go to the command line and type `npm install d3`

#### Direct download
* Go to [https://d3js.org/](https://d3js.org/)
* Download the latest version of D3.js (d3.zip)
* Unzip the file and find the minified version of the D3 source code (d3.min.js).
* Paste the file into your project's 'libraries' folder.
* Include the path to the file in the `<head>` tag of your HTML doc.

```html
<head>
	<script src = "/libraries/d3.min.js"></script>
</head>
```
 
#### CDN link
** Add the CDN link in the `<head>` of your HTML doc - [https://d3js.org/d3.v4.min.js](https://d3js.org/d3.v4.min.js)

```html
<head>
	<script src = "https://d3js.org/d3.v4.min.js"></script>
</head>
```

## SVG & SVG Elements

SVG stands for "Scalable Vector Graphics." They are perfect for D3 because SVG defines the graphics in XML format. This means that SVG images can be searched, indexed, scripted, and compressed. They can also be scaled and zoomed without losing any visual quality.

Take a look - this `<svg>` will produce a circle and a rectangle.

```html
<svg width="200" height="200">
  <circle cx="20" cy="20" r="20" fill="green" />
  <rect x="110" y="110" height="30" width="30" fill="blue" />
</svg>
```

#### SVG Group Elements: `<g>`

The SVG group element is a container used to group and contain child SVG elements. It is represented by the `<g></g>` tags, so we will refer to it from here on out as the `<g>` element. Here's what you need to know up front:

* You can nest `<g>` elements within each other.
* Because of this, all its attributes are inherited by its child elements.
* And transformations applied to a `<g>` element are performed on all of its child elements.

So let's say we want to add more circles and rectangles to the `<svg>` above. Wouldn't it be easier if we grouped all the circles and all the rectangles together?

```html
<svg width="200" height="200">
  <g>
    <circle cx="20" cy="20" r="20" fill="green" />
    <circle cx="70" cy="70" r="20" fill="purple" />
  </g>
  <g>
    <rect x="160" y="160" height="30" width="30" fill="red" />
    <rect x="110" y="110" height="30" width="30" fill="blue" />
  </g>
</svg>
```

Much easier to read, right?


Check out [this interactive example](http://www.redotheweb.com/CodeFlower/) of what you'll be able to do after learning and practicing using SVG elements with D3!

