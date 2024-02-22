# codsoft_3
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>CALCULATOR</title>
    <link rel="stylesheet" href="./calculator.css" />
  </head>

  <body>
    <section>
      <h1>Calculator</h1>

      <form>
        <input type="text" id="inp" />
      </form>

      <div id="btns">
        <button id="btn" onclick="clr()">C</button>
        <button id="btn" onclick="back()">B</button>
        <button id="btn" onclick="display('%')">%</button>
        <button id="btn" onclick="display('/')">/</button>
        <button id="btn" onclick="display(7)">7</button>
        <button id="btn" onclick="display(8)">8</button>
        <button id="btn" onclick="display(9)">9</button>
        <button id="btn" onclick="display('')"></button>
        <button id="btn" onclick="display(4)">4</button>
        <button id="btn" onclick="display(5)">5</button>
        <button id="btn" onclick="display(6)">6</button>
        <button id="btn" onclick="display('-')">-</button>
        <button id="btn" onclick="display(1)">1</button>
        <button id="btn" onclick="display(2)">2</button>
        <button id="btn" onclick="display(3)">3</button>
        <button id="btn" onclick="display('+')">+</button>
        <button id="btn" onclick="display('00')">00</button>
        <button id="btn" onclick="display(0)">0</button>
        <button id="btn" onclick="display('.')">.</button>
        <button id="btn" onclick="equal()">=</button>
      </div>
    </section>
  </body>
  <style>
    * {
      padding: 0;
      margin: 0;
      box-sizing: border-box;
    }
    body {
      width: 100vw;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      align-content: center;
    }
    section {
      display: flex;
      align-items: center;
      justify-content: center;
      align-content: center;
      flex-direction: column;
      border: 1px solid;
      background-color: darkgray;
      border-radius: 1rem;
    }
    #btns {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      padding: 1rem;
      gap: 10px;
    }
    #btn {
      padding: 1rem;
      font-size: 1.2rem;
      border-radius: 1rem;
      border: 0px;
    }
    #inp {
      width: 15rem;
      height: 3rem;
    }
    h1 {
      padding-bottom: 2rem;
      color: red;
      font-size: 3rem;
    }
    #btn:hover {
      background-color: orange;
      border: 0px;
    }
    #inp {
      font-size: 1.5rem;
    }
  </style>
  <script>
    var input = document.getElementById("inp");
    var btn = document.getElementById("btn");
    function display(num) {
      input.value = input.value + num;
    }
    function clr() {
      input.value = "";
    }
    function equal() {
      input.value = eval(inp.value);
    }
    function back() {
      input.value = input.value.slice(0, -1);
    }
  </script>
</html>
