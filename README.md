<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Be My Valentine, Bubuu ❤️</title>
  <style>
    body {
      margin: 0;
      font-family: 'Arial', sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      color: #fff;
      text-align: center;
    }
    .card {
      background: rgba(0, 0, 0, 0.25);
      padding: 30px;
      border-radius: 20px;
      width: 90%;
      max-width: 420px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.3);
    }
    h1 { font-size: 28px; margin-bottom: 10px; }
    p { font-size: 16px; }
    button {
      margin-top: 20px;
      padding: 12px 24px;
      font-size: 16px;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      background: #ff4b5c;
      color: #fff;
      transition: transform 0.2s ease, background 0.2s ease;
    }
    button:hover { transform: scale(1.05); background: #ff1e3c; }
    .hidden { display: none; }
    .heart {
      font-size: 40px;
      animation: float 1.5s infinite ease-in-out;
    }
    @keyframes float {
      0% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
      100% { transform: translateY(0); }
    }
  </style>
</head>
<body>
  <div class="card">
    <div id="startScreen">
      <h1>Hey Bubuu 💖</h1>
      <p>Ready to play a tiny Valentine game?</p>
      <button onclick="startGame()">Start Game</button>
    </div><div id="gameScreen" class="hidden">
  <p>Tap the heart to unlock a surprise 💘</p>
  <div class="heart" onclick="winGame()">❤️</div>
</div>

<div id="endScreen" class="hidden">
  <h1>Bubuu 🌹</h1>
  <p>Will you be my Valentine on 14th Feb?</p>
  <button onclick="yesClicked()">YES 💍</button>
</div>

<div id="finalScreen" class="hidden">
  <h1>YAY!! 🥰</h1>
  <p>You just made my Valentine's Day special ❤️</p>
</div>

  </div>  <script>
    function startGame() {
      document.getElementById('startScreen').classList.add('hidden');
      document.getElementById('gameScreen').classList.remove('hidden');
    }

    function winGame() {
      document.getElementById('gameScreen').classList.add('hidden');
      document.getElementById('endScreen').classList.remove('hidden');
    }

    function yesClicked() {
      document.getElementById('endScreen').classList.add('hidden');
      document.getElementById('finalScreen').classList.remove('hidden');
    }
  </script></body>
</html>
