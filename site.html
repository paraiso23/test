<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Sound Bingo Online</title>
  <style>
    body {
      font-family: "Segoe UI", sans-serif;
      background: #1d1d2f;
      color: #f5f5f5;
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      padding: 20px;
    }
    h1 { color: #ffcc00; }
    #board {
      display: grid;
      grid-template-columns: repeat(5, 80px);
      gap: 8px;
      margin: 20px 0;
    }
    .cell {
      background: #333;
      border-radius: 6px;
      width: 80px;
      height: 80px;
      display: flex;
      justify-content: center;
      align-items: center;
      cursor: pointer;
      font-size: 0.9em;
      padding: 5px;
    }
    .cell.marked {
      background: #ff6600;
      color: #fff;
      font-weight: bold;
    }
    button {
      margin: 10px;
      padding: 10px 16px;
      border: none;
      border-radius: 6px;
      background: #ffcc00;
      cursor: pointer;
      font-weight: bold;
    }
    button:hover { background: #ffaa00; }
    #message { margin-top: 15px; font-size: 1.2em; color: #00ffcc; }
  </style>
</head>
<body>
  <h1>🎶 Sound Bingo Online 🎧</h1>
  <p>Escucha el sonido y marca la palabra si está en tu tablero.</p>

  <div id="board"></div>

  <button onclick="playSound()">🔊 Reproducir sonido</button>
  <div id="current"></div>
  <div id="message"></div>

  <script>
    // Palabras y sonidos (demo con sonidos libres de beep)
    const items = [
      { word: "Microphone", sound: "https://actions.google.com/sounds/v1/alarms/beep_short.ogg" },
      { word: "Mixer", sound: "https://actions.google.com/sounds/v1/alarms/beep_short.ogg" },
      { word: "Speaker", sound: "https://actions.google.com/sounds/v1/alarms/beep_short.ogg" },
      { word: "Feedback", sound: "https://actions.google.com/sounds/v1/alarms/beep_short.ogg" },
      { word: "Gain", sound: "https://actions.google.com/sounds/v1/alarms/beep_short.ogg" },
      { word: "Equalizer", sound: "https://actions.google.com/sounds/v1/alarms/beep_short.ogg" },
      { word: "Headphones", sound: "https://actions.google.com/sounds/v1/alarms/beep_short.ogg" },
      { word: "Amplifier", sound: "https://actions.google.com/sounds/v1/alarms/beep_short.ogg" },
      { word: "Stage", sound: "https://actions.google.com/sounds/v1/alarms/beep_short.ogg" },
      { word: "Monitor", sound: "https://actions.google.com/sounds/v1/alarms/beep_short.ogg" }
    ];

    // Estado
    let board = [];
    let used = [];
    const boardContainer = document.getElementById("board");
    const current = document.getElementById("current");
    const message = document.getElementById("message");

    function shuffle(arr) {
      return arr.sort(() => Math.random() - 0.5);
    }

    function initBoard() {
      const shuffled = shuffle([...items]).slice(0, 25);
      board = shuffled.map(x => x.word);
      boardContainer.innerHTML = "";
      board.forEach((w, idx) => {
        const cell = document.createElement("div");
        cell.className = "cell";
        cell.textContent = w;
        cell.onclick = () => toggleMark(cell, idx);
        boardContainer.appendChild(cell);
      });
    }

    function toggleMark(cell, idx) {
      cell.classList.toggle("marked");
      checkBingo();
    }

    function playSound() {
      if (used.length === items.length) {
        message.textContent = "Ya se reprodujeron todos los sonidos.";
        return;
      }
      let choice;
      do {
        choice = items[Math.floor(Math.random() * items.length)];
      } while (used.includes(choice.word));
      used.push(choice.word);

      const audio = new Audio(choice.sound);
      audio.play();
      current.textContent = `👉 Palabra: ${choice.word}`;
    }

    function checkBingo() {
      const cells = document.querySelectorAll(".cell");
      const marked = Array.from(cells).map(c => c.classList.contains("marked"));

      // Rejilla 5x5
      for (let r = 0; r < 5; r++) {
        if (marked.slice(r*5, r*5+5).every(Boolean)) {
          message.textContent = "🎉 ¡Bingo en fila!";
          return;
        }
      }
      for (let c = 0; c < 5; c++) {
        if ([0,1,2,3,4].map(r => marked[r*5+c]).every(Boolean)) {
          message.textContent = "🎉 ¡Bingo en columna!";
          return;
        }
      }
      if ([0,6,12,18,24].every(i => marked[i])) {
        message.textContent = "🎉 ¡Bingo en diagonal!";
        return;
      }
      if ([4,8,12,16,20].every(i => marked[i])) {
        message.textContent = "🎉 ¡Bingo en diagonal!";
        return;
      }
    }

    initBoard();
  </script>
</body>
</html>
