<!---
{"next":"Topics/resources.md","title":"D3 Scales"}
-->

# D3 Scales

## [Applying Scales](https://codepen.io/mottaquikarim/pen/xeLjbx?editors=0010)

<p class="codepen" data-height="300" data-theme-id="820" data-default-tab="js,result" data-user="mottaquikarim" data-slug-hash="xeLjbx" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid black; margin: 1em 0; padding: 1em;" data-pen-title="D3/React - Applying Scales - Code Along  - 9/8">
  <span>See the Pen <a href="https://codepen.io/mottaquikarim/pen/xeLjbx/">
  D3/React - Applying Scales - Code Along  - 9/8</a> by Mottaqui Karim (<a href="https://codepen.io/mottaquikarim">@mottaquikarim</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

## Code

```javascript
//let data = [ 0, 2, 3, 7.5, 9, 10 ]
let data = [ 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17 ]

let width = 460
let height = 80
// Continuous Input and Output
// d3.scaleLinear()
let scaleLinearX = d3.scaleLinear()
  .domain(d3.extent(data, d => d))
  .range([40,width])

let scaleLinearY = d3.scaleLinear()
  .domain([d3.min(data, d => d), d3.max(data, d => d)])
  .range([height, 20])

let scaleLinearColor = d3.scaleLinear()
  .domain([0, d3.max(data, d => d)])
  .range(['lightblue', 'lightgreen'])

// d3.scaleSequential()
let scaleSequential = d3.scaleSequential(d3.interpolatePiYG)
  .domain([0,data.length-1])

// Continuous Input and Discrete Output
// d3.scaleQuantize()
let scaleQuanitize = d3.scaleQuantize()
  .domain([0,20])
  .range(['lightblue', 'orange', 'lightgreen', 'pink']);

// Discrete Input and Discrete Output
// d3.scaleOrdinal()
// let scaleOrdinal = d3.scaleOrdinal(d3.schemeBlues[3])
//   .domain([d3.extent(data => d)])
  // .range(['lightblue', 'lightgreen'])
// d3.scaleBand()

let scaleBand = d3.scaleBand()
  .domain(d3.range(data.length))
  .range([20, 480])
  .paddingInner(0.05)

let svg = d3.select('#root').append('svg')
  .attr('width', 500).attr('height',100)
// DATA BINDING
let rects = svg.selectAll('rects').data(data)
// ENTER
rects.enter()
  .append('rect')
  .attr('x', (d,i) => scaleBand(i))
  .attr('y', d => scaleLinearY(d))
  .attr('width', scaleBand.bandwidth())
  .attr('height', d => 90 - scaleLinearY(d))
  // .style('fill', d => scaleQuanitize(d))
  //  .style('fill', d => scaleOrdinal(d))
  // .style('fill', d => scaleSequential(d))
  .style('fill', d => scaleLinearColor(d))

```

