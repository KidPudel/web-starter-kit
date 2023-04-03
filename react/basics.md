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

# State
State is simply a javascript Object

# hooks
Hooks are functions that let you "_hook into_" state and lifecycle features.  
In other words hooks let us add state into functional component.  
Hooks are functions that start with `use`.  
Hooks are more restrictive that other functions.  

> Rules: 
> 1. hooks don't work inside classes - they let you use React without classes
> 2. hooks called only at the top of the component

```ts
let [fruits, setFruits] = useState([]);

let getFruits = async () => {
    let response = await http.fetch("fruits/");
    let fruits = await response.json();
    setFruits(fruits)
}
```

# useState

_**Defenition**_: Hook function that leting you to manage state of the variable. They handle the data that changes over time. So when data changes - re-render the UI

**_Returns_**: the hook is just a function that returns a value (reactive state) as well as a function to change a value (setter)

**_Parameters_**: _**useState can take initial state as a parameter**_

```js
const [count, setCount] = setState(0);

return (
    <p>{count}</p>
    <button onClick= { () => setCount(count + 1) }>Count</button>
)

```

# useEffect
function that allows us to manage our component lifecycle

---

## Component lyfecycle
1. Mounted (initialized)
2. Updated (state updated)
3. Unmounted (destryed)

---

This code will be runned when:
1. Mounted
2. Updated
```ts
useEffect(() => {
    alert("hello!")
}
```

But what if we want to fetch something when component is first initialized?  
```ts
let [loaded, setLoaded] = useState(false);
useEffect(() => {
    fetch('foo').then(() => setLoaded(true)) // re-rendering loop 👎
})
```
Well that's bad, because then we will fetch something everytime when our state is changed and therefore change the state again and re-render it againt and..  
In other words - that is bad.  

The solution is to add the second parameter - **_dependencies_**
```ts
let [loaded, setLoaded] = useState(false);
useEffect(() => {
    fetch('foo').then(() => setLoaded(true)) // re-rendering loop 👎
}, [])
```
if _dependencies_ are empty, then our useEffect will be called only on when it first initializes.  
Or we can add dependencies - on which state update (re-render) `useEffect()` is going to be called.  

And the last thing for `useEffect()` is we can do something "on destroy" of component:
```ts
let [loaded, setLoaded] = useState(false);
useEffect(() => {
    fetch('foo').then(() => setLoaded(true)) // re-rendering loop 👎
    
    return () => alert("goodbye, component 👋")
}, [])
```

# useContext
context - share data without passing props.  

Usage: Allow us access or consume current value from context provider which could be many layers higher
```ts
const moods = [
    happy: '😃'
    sad: '☹️'
]

const MoodContext = createContext(moods);

export default function App(props) {
    return (
        <MoodContext.Provider value={mood.happy}>
            <MoodEmoji />
        </MoodContext.Provider>
            
    )
}


function MoodEmoji() {
    const mood = useContext(MoodContext);
    
    return (
        <p>
            {mood.happy}
        </p>
    )
}

```
`useContext()` basically a cleaner replacement for a context `Consumer`

```ts
function MoodEmoji() {
    return (
        <MoodContext.Context>
            { ({mood}) => { <p> {mood} </p>} }
        </MoodContext.Context>
            
    )
}


```
