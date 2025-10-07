# MWAD-EXP_04-Simple-caluculator
## Date:

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
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
## Calculator.js
```
import React, { useState } from "react";
import "./Calculator.css";

const Calculator = () => {
  const [input, setInput] = useState("");

  // Handle button click
  const handleClick = (value) => {
    if (value === "C") {
      setInput("");
    } else if (value === "=") {
      try {
        // Evaluate the expression safely
        setInput(eval(input).toString());
      } catch (error) {
        setInput("Error");
      }
    } else {
      setInput(input + value);
    }
  };

  // Calculator buttons
  const buttons = [
    "C", "/", "*", "7",
    "8", "9", "-", "4",
    "5", "6", "+", "1",
    "2", "3", "0", ".",
    "="
  ];

  return (
    <div className="calculator-container">
      <div className="calculator">
        <div className="display">{input || "0"}</div>
        <div className="buttons">
          {buttons.map((btn, index) => (
            <button
              key={index}
              className={`button ${btn === "=" ? "equal" : ""} ${btn === "C" ? "clear" : ""}`}
              onClick={() => handleClick(btn)}
            >
              {btn}
            </button>
          ))}
        </div>
      </div>
      <div className="credits">
        <p>DEVELOPED BY: AMIRTHAVARSHINI V</p>
        <p>REGISTER NUMBER: 212223040014</p>
      </div>
    </div>
  );
};

export default Calculator;
```
## Calculator.css
```
/* Container for centering */
.calculator-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 50px;
  font-family: 'Arial', sans-serif;
}

/* Calculator frame */
.calculator {
  background-color: #d3d3d3; /* neutral grey */
  padding: 20px;
  border-radius: 15px;
  box-shadow: 0px 5px 15px rgba(0,0,0,0.3);
  width: 280px;
}

/* Display screen */
.display {
  background-color: #f0f0f0;
  color: #000;
  font-size: 2rem;
  padding: 15px;
  margin-bottom: 20px;
  border-radius: 10px;
  text-align: right;
  min-height: 50px;
  box-shadow: inset 0px 2px 4px rgba(0,0,0,0.2);
  overflow-x: auto;
}

/* Buttons grid */
.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 10px;
}

/* Button style */
.button {
  padding: 15px;
  font-size: 1.2rem;
  border: none;
  border-radius: 10px;
  cursor: pointer;
  background-color: #e0e0e0;
  transition: all 0.2s ease;
}

.button:hover {
  background-color: #c0c0c0;
}

/* Special buttons */
.equal {
  background-color: #4caf50;
  color: white;
  grid-column: span 2;
}

.equal:hover {
  background-color: #45a049;
}

.clear {
  background-color: #f44336;
  color: white;
}

.clear:hover {
  background-color: #da190b;
}

/* Credits */
.credits {
  margin-top: 20px;
  text-align: center;
  font-size: 0.9rem;
  color: #333;
}
```
## App.js
```
import React from "react";
import Calculator from "./Calculator";

function App() {
  return <Calculator />;
}

export default App;
```

## OUTPUT

<img width="1919" height="1123" alt="image" src="https://github.com/user-attachments/assets/c554ce51-960f-4db1-9620-78fb0b486bc6" />




## RESULT
The program for developing a simple calculator in React.js is executed successfully.
