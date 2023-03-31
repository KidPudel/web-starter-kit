```tsx
import React from "react";
import logo from "./logo.svg";
import "./App.css";
import Pin from "./components/Pin"

function App() {
  let gesture: string = "🤟";

  return (
    <div className="App">
      <div className="inner-div">
        <Pin title="Adventure time" description="adventure time pin" />
      </div>
    </div>
  );
}

export default App;

```

```tsx
import { Box, Card } from "@mui/material";


export default function Pin({ title, description }: {
    title: string;
    description: string;
}) {
    return (
        <Card elevation={15} className="Pin-card">
            <Box>
                <h1 >
                    {title}
                </h1>
                <p>
                    {description}
                </p>
            </Box>
        </Card>
    )
}
```


```css
html, body {
  height: 100%;
  margin: 0;
}


.inner-div {
  min-height: 100vh; 
  min-width: 100vw;
  background-color: blueviolet;
  display: flex;
  justify-content: center;
  align-items: center;
}


.Pin-card {
  width: 300px;
  height: 200px;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
} 
```
