<!DOCTYPE html><html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Игра</title>
  <style>
    body {
      background-color: black;
      color: white;
      font-family: Arial, sans-serif;
      text-align: center;
      margin: 0;
      padding: 0;
    }
    h1 {
      margin-top: 20px;
    }
    .buttons {
      margin: 20px;
    }
    button {
      background-color: white;
      color: black;
      border: none;
      padding: 10px 20px;
      font-size: 16px;
      margin: 10px;
      cursor: pointer;
      border-radius: 8px;
    }
    #game-board {
      display: none;
      margin-top: 20px;
    }
    .row {
      display: flex;
      justify-content: center;
    }
    .cell {
      width: 60px;
      height: 60px;
      border: 2px solid white;
      margin: 5px;
      font-size: 32px;
      line-height: 60px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h1>Игра сделана с ChatGPT</h1>
  <div class="buttons">
    <button onclick="buyPro()">Pro</button>
    <button onclick="startGame()">Play</button>
  </div>  <div id="game-board">
    <div class="row">
      <div class="cell" onclick="makeMove(this)"></div>
      <div class="cell" onclick="makeMove(this)"></div>
      <div class="cell" onclick="makeMove(this)"></div>
    </div>
    <div class="row">
      <div class="cell" onclick="makeMove(this)"></div>
      <div class="cell" onclick="makeMove(this)"></div>
      <div class="cell" onclick="makeMove(this)"></div>
    </div>
    <div class="row">
      <div class="cell" onclick="makeMove(this)"></div>
      <div class="cell" onclick="makeMove(this)"></div>
      <div class="cell" onclick="makeMove(this)"></div>
    </div>
  </div>  <script>
    let currentPlayer = 'X';

    function startGame() {
      document.getElementById('game-board').style.display = 'block';
    }

    function buyPro() {
      alert('Покупка премиума за 20 гривен (фиктивно)');
    }

    function makeMove(cell) {
      if (cell.innerText === '') {
        cell.innerText = currentPlayer;
        currentPlayer = currentPlayer === 'X' ? 'O' : 'X';
      }
    }
  </script></body>
</html>
