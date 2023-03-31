```tsx
import React from "react";
import logo from "./logo.svg";
import "./App.css";

import { Pin } from "./components/Pin"


function App() {
  let gesture: string = "🤟";

  return (
    <div className="App">
      <div className="nested-window">
        <Pin title="Adventure Time " description="adventure time pin" />
      </div>
    </div>
  );
}

export default App;

```

```css
* {
  box-sizing: border-box;
  overflow: hidden;
}


.App {
  min-height: 100vh;
  background-color: pink;
  display: flex;
  padding: 5px; 
}

.nested-window {
  background-color: blueviolet;
  border: 5px solid black;
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;

}

.Pin {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  border: 2px solid black;
}


```


```tsx
import { Card, CardContent, CardMedia } from "@mui/material";

export function Pin({ title, description }: {
    title: string;
    description: string
}) {
    return (
        <Card className="Pin" sx={{ boxShadow: "5px 10px" }}>
            <CardMedia
                component="img"
                height="140"
                image="https://media.npr.org/assets/img/2013/06/16/fj_princesses_300_wide-f84adf6c953c93c422186bf6d470612c6bc50145-s900-c85.webp"
                alt="adventure time" />
            <CardContent>
                <h1>
                    {title}
                </h1>
                <p>
                    {description}
                </p>

            </CardContent>
        </Card>
    )
}

export { Card };
```
