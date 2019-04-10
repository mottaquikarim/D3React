<!---
{"next":"Topics/d3_libelem.md","title":"Core Features & Applications"}
-->

# Core Features & Applications

## What is D3?
- JavaScript library for building Data Visualizations
- Most widely used Data Viz JS library
- APIs and charting elements to transform and map your data to construct detailed and engaging graphics.
- Most recent release is D3v5 which introduced only a small handful of changes

## D3's Strengths
- Data Binding: .data(dataset)  
- Enter/Update/Exit Methodology:  .enter()  / .exit() / .merge()
- Scales: d3.scaleLinear() / d3.scaleOrdinal() / d3.scaleBand() 
- Axes: d3.axisBottom() / d3.axisTop()
- Generators: d3.line() / d3.pie() / d3.arc()
- Layouts: / d3.force()  / d3.tree() / d3.partition()

## What is React?
- JavaScript library for building user interfaces
- Build reusable components to use throughout your application 
- Use a one-directional data-flow to pass information into components
- React components will re-render based on their lifecycle 
- Written in JSX / ES6

## React's Strengths
  - Reusable Components
  - Component Lifecycle Methods (componentDidMount, componentDidUpdate)
  - Passing Data Down as Props 
  - Updating State to initialize a re-render 
  - React Ecosystem (Redux, React Router, etc.)

## Why use React?
*Why structure your code with a framework?*

- **Separation of concerns**: abstract your visualization code from data management
- **Reusability**: create components that you can use throughout / across projects
- **Reliability**: other people have written more reliable code that triggers updates

*Why use the __React__ framework?*
- **Popularity**: quickly evolving, large open source community
- **Data centric**: based on a philosophy of observing data updates

## React + D3 - Who does what?

#### React
- Manage data, keep track of settings (i.e., what data to visualize)
- Append static elements to the DOM (i.e., <g> elements that hold circles)

#### D3
- Compute visual layouts
- Render elements that are based on binding data to DOM (i.e., circles)
	"Highly contested", may depend on type of app, team, data size, etc.

