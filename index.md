---
layout: default
title: Student Blog
---

## Tejas' Blog 

## About Me:
My name is Tejas and I'm a sophomore at Del Norte High School. I like basketball, boba, and I live in California. I took this class because it's challenging, and seemed like it would be fun.

<img src="images/freeform.png"  width="300" height="500">

## Me!
<img src="images/hawaiime.JPG"  width="200" height="250">

## My Schedule

| Period      | Class |
| ----------- | ---------- |
|1    | AP Computer Science       |
|2    | AP Calculus        |
|3    | AP World History       |
|4    | Honors Humanities        |
|5    | AP Biology        |

## Go to My Page:
This is my [Github page](https://github.com/TejM123){:target="_blank"}!

## Hacks

Run bundle install where the Gemfile is located. Then download PyYaml and nbconvert which will run your make command. Copy the link after running make command. The file to edit the blog is index.md. You can also use the notebooks to create other blogs to edit to your liking. You can use ls to list all the files in a directory. Use cd to switch between directories. You use pip3 install to download. mkdir helps you make a directory. In order to check your version number, type "software name" --version.


## Calculator

<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
  body {
    font-family: Arial, sans-serif;
  }

  .calculator {
    width: 250px;
    border: 1px solid #ccc;
    padding: 10px;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
    margin: 0 auto;
  }

  .output {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    font-size: 24px;
    margin-bottom: 10px;
  }

  .buttons {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-gap: 5px;
  }

  button {
    padding: 10px;
    font-size: 18px;
    background-color: #f0f0f0;
    border: none;
    cursor: pointer;
  }
button:hover {
    background-color: #d0d0d0;
  }
</style>
<title>Calculator</title>
</head>
<body>
  <div class="calculator">
    <div class="output" id="output">0</div>
    <div class="buttons">
      <button onclick="appendToOutput('7')">7</button>
      <button onclick="appendToOutput('8')">8</button>
      <button onclick="appendToOutput('9')">9</button>
      <button onclick="appendToOutput('+')">+</button>
      <button onclick="appendToOutput('4')">4</button>
      <button onclick="appendToOutput('5')">5</button>
      <button onclick="appendToOutput('6')">6</button>
      <button onclick="appendToOutput('-')">-</button>
      <button onclick="appendToOutput('1')">1</button>
      <button onclick="appendToOutput('2')">2</button>
      <button onclick="appendToOutput('3')">3</button>
      <button onclick="appendToOutput('*')">x</button>
      <button onclick="appendToOutput('0')">0</button>
      <button onclick="calculate()">=</button>
      <button onclick="clearOutput()">C</button>
      <button onclick="appendToOutput('/')">/</button>
</div>
  </div>

  <script>
    let outputElement = document.getElementById('output');
    let currentInput = '';

    function appendToOutput(value) {
      currentInput += value;
      outputElement.innerText = currentInput;
    }

    function calculate() {
      try {
        currentInput = eval(currentInput).toString();
        outputElement.innerText = currentInput;
      } catch (error) {
        outputElement.innerText = 'Error';
      }
    }

    function clearOutput() {
      currentInput = '';
      outputElement.innerText = '0';
    }
  </script>
</body>