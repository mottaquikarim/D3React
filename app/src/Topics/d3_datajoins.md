<!---
{"next":"Topics/d3_scales.md","title":"D3 Data Joins"}
-->

# D3 Data Joins

`selection.join(enter[, update][, exit])`

This method appends, removes and reorders elements as necessary to match the data that was previously bound by selection.data. It returns the merged enter and update selection.

```javascript
// Your starting selection
svg.selectAll("circle")
  .data(data)
  .join("circle")
    .attr("fill", "none")
    .attr("stroke", "black");

// Joining the data
svg.selectAll("circle")
  .data(data)
  .join(
    enter => enter.append("circle").attr("fill", "green"),
    update => update.attr("fill", "blue")
  )
    .attr("stroke", "black");
```


## D3 Code Along 2 - Data Import & Binding

[Go here](https://codepen.io/mottaquikarim/pen/WWEzWM?editors=0010).

<p class="codepen" data-height="300" data-theme-id="820" data-default-tab="js,result" data-user="mottaquikarim" data-slug-hash="WWEzWM" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid black; margin: 1em 0; padding: 1em;" data-pen-title="D3 Basics - Data Import and Binding -  Code Along  - 9/8">
  <span>See the Pen <a href="https://codepen.io/mottaquikarim/pen/WWEzWM/">
  D3 Basics - Data Import and Binding -  Code Along  - 9/8</a> by Mottaqui Karim (<a href="https://codepen.io/mottaquikarim">@mottaquikarim</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

## D3 Code Along 3 - Selections & Events

[Go here](https://codepen.io/mottaquikarim/full/bJrvya).

<p class="codepen" data-height="300" data-theme-id="820" data-default-tab="html,result" data-user="mottaquikarim" data-slug-hash="bJrvya" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid black; margin: 1em 0; padding: 1em;" data-pen-title="D3 - Basics - Selections and Events - Lab - 9/8">
  <span>See the Pen <a href="https://codepen.io/mottaquikarim/pen/bJrvya/">
  D3 - Basics - Selections and Events - Lab - 9/8</a> by Mottaqui Karim (<a href="https://codepen.io/mottaquikarim">@mottaquikarim</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>