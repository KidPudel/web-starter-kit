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


# props
Props are letting you to access variables

# hooks
Hools leting you to manage state of the variable (create internal state)

the hook is just a function that returns a value as well as a function to change a value

```js
const [count, setCount] = setState(0);

return (
    <p>{count}</p>
    <button onClick= { () => setCount(count + 1) }></button>
)

```
