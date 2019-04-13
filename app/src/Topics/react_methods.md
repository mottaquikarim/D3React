<!---
{"next":"Topics/react_lifecycle_methods.md","title":"Creating Methods in React"}
-->

# Creating Methods in React

```javascript
class Button extends Component {
	constructor(props) {
		super(props)
		this.state = {
			label: "Hello, Wrold",
			toggle: false,
		}
	}

	onClick = e => {
		let {toggle, label} = this.state;
		if (toggle) {
			label = 'Goodbye, Wrold'
		}
		else {
			label = 'Hello, Wrold'
		}
		toggle = !toggle

		this.setState({toggle, label})
	}

	render() {

		return <button onClick={e => this.onClick}>{toggle}</button>
	}
}
```