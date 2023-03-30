React is a front-end component based (reusable!!) framework  

# Component

Component is just a function ! :)
And the return type of this function is html or UI which is written in `jsx/tsx` syntax (js + html)

```typescript
import React from 'react';
import logo from './logo.svg';
import './App.css';

function App() {
  let gesture: string = "🤟"

  return (
      <h1 className='Hello'>Hello React!! {gesture}</h1>
  );
}

export default App;
```

```css
.Hello {
  text-align: center;
}
```
![image](https://user-images.githubusercontent.com/63263301/228927180-56e22d27-6364-4e0f-b27c-e9f93ee13bf8.png)


# props (short from properties)
**_In React, "props" (short for "properties") is a way to pass data and information between components. Props are used to provide information to a component from its parent component, allowing the child component to render based on the data passed in._**

_Props are passed as attributes to a component in JSX, and can be accessed within the component using the props object. The **props object contains key-value pairs** of the attributes passed to the component, where the key is the attribute name and the value is the attribute value.__

For example, consider the following code:

```js
function MyComponent(props) {
  return <div>{props.name}</div>;
}

<MyComponent name="John" />
```

In this example, the `MyComponent` component is passed a `name` prop with a value of "John". Within the component, the `name` prop is accessed using `props.name` and is used to render the name in a `<div>` element.

Props are an essential concept in React and are used extensively to create dynamic and reusable components.

# hooks
Hools leting you to manage state of the variable (create internal state)

the hook is just a function that returns a value as well as a function to change a value

```js
const [count, setCount] = setState(0);

return (
    <p>{count}</p>
    <button onClick= { () => setCount(count + 1) }>Count</button>
)

```
