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
    <div className='App'>
      <h1 className='App-greeting'>Hello React!! {gesture}</h1>
    </div>
  );
}

export default App;

``
