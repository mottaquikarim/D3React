<!---
{"next":"Topics/d3_scales.md","title":"D3 Data Joins"}
-->

# D3 Data Joins


`selection.data([data[, key]])`

```javascript
d3.select("body")
  .append("table")
  .selectAll("tr")
  .data(matrix)
  .join("tr")
  .selectAll("td")
  .data(d => d)
  .join("td")
    .text(d => d);
```

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

[Go here](https://codepen.io/jkeohan/pen/rZYRzL?editors=0010).

## D3 Code Along 3 - Selections & Events

[Go here](https://codepen.io/jkeohan/pen/YOEOXB?editors=0010).