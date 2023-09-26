---
toc: true
comments: false
layout: post
title: Calculator
description: A basic calculator
type: hacks
courses: { compsci: {week: 2} }
---

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Calculator</title>
<style>
  body {
    margin: 0;
    padding: 0;
    background-image: url('cool-background.jpg'); /* Replace with your image URL */
    background-size: cover;
    font-family: Arial, sans-serif;
  }
  .calculator {
    width: 300px;
    margin: 100px auto;
    padding: 20px;
    background-color: rgba(255, 255, 255, 0.7);
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  }
  input[type="text"] {
    width: 100%;
    padding: 10px;
    margin-bottom: 10px;
    font-size: 18px;
    border: none;
    border-radius: 5px;
  }
  button {
    width: 50px;
    height: 50px;
    font-size: 20px;
    margin: 5px;
    border: none;
    border-radius: 5px;
    background-color: #3498db;
    color: #fff;
    cursor: pointer;
  }
</style>
</head>
<body>
  <div class="calculator">
    <input type="text" id="result" readonly>
    <table>
      <tr>
        <td><button onclick="appendToResult('7')">7</button></td>
        <td><button onclick="appendToResult('8')">8</button></td>
        <td><button onclick="appendToResult('9')">9</button></td>
        <td><button onclick="appendToResult('+')">+</button></td>
      </tr>
      <tr>
        <td><button onclick="appendToResult('4')">4</button></td>
        <td><button onclick="appendToResult('5')">5</button></td>
        <td><button onclick="appendToResult('6')">6</button></td>
        <td><button onclick="appendToResult('-')">-</button></td>
      </tr>
      <tr>
        <td><button onclick="appendToResult('1')">1</button></td>
        <td><button onclick="appendToResult('2')">2</button></td>
        <td><button onclick="appendToResult('3')">3</button></td>
        <td><button onclick="appendToResult('*')">*</button></td>
      </tr>
      <tr>
        <td><button onclick="appendToResult('0')">0</button></td>
        <td><button onclick="clearResult()">C</button></td>
        <td><button onclick="calculateResult()">=</button></td>
        <td><button onclick="appendToResult('/')">/</button></td>
      </tr>
    </table>
  </div>
  
  <script>
    function appendToResult(value) {
      document.getElementById('result').value += value;
    }
    
    function clearResult() {
      document.getElementById('result').value = '';
    }
    
    function calculateResult() {
      try {
        const result = eval(document.getElementById('result').value);
        document.getElementById('result').value = result;
      } catch (error) {
        document.getElementById('result').value = 'Error';
      }
    }
  </script>
</body>
</html>
