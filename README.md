# EXPERIMENT 06: DEVELOP A SIMPLE CALCULATOR USING REACT FRAMEWORK
## AIM:
To develop a simple calculator using react framework.
## ALGORTIHM:
1. Cretae a new react project named todolist.
2. Import required hooks from the react.
3. Program the function App() with required components.
4. Export the default app at the end of function component.
5. Add required styling to the component.
6. Display the project using the command npm start.
## PROGRAM:
```
DEVELOPED BY:RITHIGAS SRI.B
REGISTER NUMBER:212221230083
```
### App.js:
```
import React, { useState } from 'react';
import './App.css';

function App() {
  const [result, setResult] = useState('');

  const handleClick = (e) => {
    setResult(result.concat(e.target.name));
  };

  const handleClear = () => {
    setResult('');
  };

  const handleCalculate = () => {
    try {
      setResult(eval(result).toString());
    } catch (error) {
      setResult('Error');
    }
  };

  return (
    <body>
      <p>SIMPLE CALCULATOR</p>
      <div className="calculator">
        <input type="text" value={result} readOnly />
        <div className="keypad">
          <button name="7" onClick={handleClick}>7</button>
          <button name="8" onClick={handleClick}>8</button>
          <button name="9" onClick={handleClick}>9</button>
          <button className="operator" name="/" onClick={handleClick}>&divide;</button>
          <button name="4" onClick={handleClick}>4</button>
          <button name="5" onClick={handleClick}>5</button>
          <button name="6" onClick={handleClick}>6</button>
          <button className="operator" name="*" onClick={handleClick}>&times;</button>
          <button name="1" onClick={handleClick}>1</button>
          <button name="2" onClick={handleClick}>2</button>
          <button name="3" onClick={handleClick}>3</button>
          <button className="operator" name="-" onClick={handleClick}>&ndash;</button>
          <button name="0" onClick={handleClick}>0</button>
          <button name="." onClick={handleClick}>.</button>
          <button className="operator" id="equals" onClick={handleCalculate}>=</button>
          <button className="operator" name="%" onClick={handleClick}>%</button>
          <button className="operator clear" onClick={handleClear}>Clear</button>
        </div>
      </div>
    </body>
  );
}

export default App;
```
### App.css
```
.calculator {
  width: 300px;
  margin: 50px auto;
  background-color: #f1f1f1;
  padding: 20px;
  border-radius: 5px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
}
body{
  background-color: black;
  margin:200px;
}
p{
  color:white;
  text-align:center;
  font-size:40px;
  font-weight:700;
}

input[type="text"] {
  width: 100%;
  height: 40px;
  margin-bottom: 10px;
  font-size: 18px;
  padding: 5px;
}

.keypad {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 5px;
}

button {
  width: 100%;
  height: 40px;
  font-size: 18px;
  border: none;
  background-color: #fff;
  cursor: pointer;
}

.operator {
  background-color: #f5923e;
  color: #fff;
}

#equals {
  background-color: #4caf50;
  color: #fff;
}
.operator.clear {
  grid-column: span 4;
}
```

## OUTPUT:
![image](https://github.com/Rithigasri/Calculator-React/assets/93427256/7b224e0b-bf2f-404b-9aa6-04f49b3f17a9)<br/>
![image](https://github.com/Rithigasri/Calculator-React/assets/93427256/62a13288-d563-4fa2-aa07-c9d3189bf191)
![image](https://github.com/Rithigasri/Calculator-React/assets/93427256/84987e2b-7849-4d6e-9848-7da01fc17d6c)

## RESULT:
Thus, a simple calculator is developed using react framework.


