<!---
{"next":"Topics/react_methods.md","title":"Passing Props in React"}
-->

# Passing Props in React

```javascript
const SomeComp = props => {
	const {foo} = props;
	return <div>Hello {foo}</div>
}

<SomeComp foo="Taq" />
```