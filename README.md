# Ex04 Simple Calculator - React Project
## Date:24-08-2026
## Name:RACHITHA U 
## Reg No :212225220078

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open htt/://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
App.jsx:
```
import { useState } from "react";
import "./App.css";

function App() {
  const [display, setDisplay] = useState("");

  const handleClick = (value) => {
    setDisplay(display + value);
  };

  const calculate = () => {
    try {
      setDisplay(eval(display).toString());
    } catch {
      setDisplay("Error");
    }
  };

  const clear = () => {
    setDisplay("");
  };

  return (
    <div className="calculator">
      <input type="text" value={display} readOnly />

      <div className="buttons">
        <button onClick={clear}>C</button>
        <button onClick={() => handleClick("/")}>÷</button>
        <button onClick={() => handleClick("*")}>×</button>
        <button onClick={() => handleClick("-")}>−</button>

        <button onClick={() => handleClick("7")}>7</button>
        <button onClick={() => handleClick("8")}>8</button>
        <button onClick={() => handleClick("9")}>9</button>
        <button onClick={() => handleClick("+")}>+</button>

        <button onClick={() => handleClick("4")}>4</button>
        <button onClick={() => handleClick("5")}>5</button>
        <button onClick={() => handleClick("6")}>6</button>
        <button onClick={() => handleClick("0")}>0</button>

        <button onClick={() => handleClick("1")}>1</button>
        <button onClick={() => handleClick("2")}>2</button>
        <button onClick={() => handleClick("3")}>3</button>
        <button onClick={calculate}>=</button>
      </div>
    </div>
  );
}

export default App;
```
App.css:
```
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html,
body,
#root {
  width: 100%;
  min-height: 100vh;
}

body {
  font-family: "Segoe UI", Arial, sans-serif;
  background: #111827;
}

#root {
  display: flex;
  justify-content: center;
  align-items: center;
}

.calculator {
  width: 330px;
  padding: 24px;
  border-radius: 22px;
  background: #1f2937;
  box-shadow: 0 20px 50px rgba(0, 0, 0, 0.45);
}

input {
  width: 100%;
  height: 75px;
  margin-bottom: 18px;
  padding: 10px 15px;
  border: none;
  border-radius: 14px;
  outline: none;
  background: #111827;
  color: #f8fafc;
  font-size: 30px;
  text-align: right;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  height: 58px;
  border: none;
  border-radius: 12px;
  background: #374151;
  color: #e5e7eb;
  font-size: 19px;
  font-weight: 600;
  cursor: pointer;
  transition: 0.2s ease;
}

button:hover {
  background: #4b5563;
}

button:active {
  transform: scale(0.95);
}

/* Clear */
button:first-child {
  background: #3f3034;
  color: #e5a5ad;
}

button:first-child:hover {
  background: #543b40;
}

/* Operators */
button:nth-child(2),
button:nth-child(3),
button:nth-child(4),
button:nth-child(8) {
  background: #293f56;
  color: #9fc5e8;
}

button:nth-child(2):hover,
button:nth-child(3):hover,
button:nth-child(4):hover,
button:nth-child(8):hover {
  background: #34516e;
}

/* Equal */
button:nth-child(16) {
  background: #2563eb;
  color: white;
}

button:nth-child(16):hover {
  background: #1d4ed8;
}
```

## OUTPUT

![alt text](<Screenshot 2026-08-24 104409.png>)

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
