<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Sorry Suvecha 🥺❤️</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to top right, #ffe0ec, #ffd6e8);
      color: #333;
      text-align: center;
      padding: 30px;
    }
    nav a {
      margin: 10px;
      text-decoration: none;
      color: #e60073;
      font-weight: bold;
      font-size: 1.1rem;
    }
    nav {
      margin-bottom: 30px;
    }
    h1 {
      font-size: 2.5rem;
      color: #e60073;
      margin-bottom: 1rem;
    }
    p, li {
      font-size: 1.2rem;
      max-width: 700px;
      margin: 0 auto 1rem;
    }
    .game-button, button {
      background-color: #ff5c8d;
      color: white;
      border: none;
      padding: 12px 20px;
      font-size: 1rem;
      border-radius: 12px;
      cursor: pointer;
      margin: 10px;
    }
    .hidden {
      display: none;
    }
  </style>
</head>
<body>
  <nav>
    <a href="#home" onclick="showPage('home')">Home</a>
    <a href="#game" onclick="showPage('game')">Emoji Game</a>
    <a href="#message" onclick="showPage('message')">My Feelings</a>
  </nav>

  <div id="home">
    <h1>I'm Sorry, Suvecha 🥺❤️</h1>
    <p>Molai maaf gardinuu, Suvecha. Mistakely bhayeko kura haru le timilai dukh diyeko chu bhanera dherai guilty feel gardai chu. Ma dherai maya garchu timilai. 💖</p>
  </div>

  <div id="game" class="hidden">
    <h1>Guess the Emotion 🧠✨</h1>
    <p>Try to guess which feeling this emoji represents!</p>
    <p id="emoji">😔</p>
    <button class="game-button" onclick="nextEmoji()">Next</button>
  </div>

  <div id="message" class="hidden">
    <h1>From My Heart 💌</h1>
    <p>
      Timi bina sabai khali lagchha. Timi mero sabai hau—musu, hasi, santwana, peace, happiness, and love.
      Tyo sound wala kura accidentally bhayo. Maile janera kehi gareko thiena. Tara tyo kura le timilai hurt gare jasto cha bhanera ma dherai sorry chu.🥺
    </p>
    <p>
      Mero feelings haru sabda ma rakhera bhanna garo cha. Tara yo website ma jati pani words cha, sabai timi ko lagi ho. Timi mero world hau, ma aaba dhyan diyera, careful bhayera, bujhera maya garxu. ❤️
    </p>
    <p>
      Please come back with that cute smile again... timro muskan mero sansar ho. 🌍💖
    </p>
  </div>

  <script>
    const emojis = ["😔", "😭", "🥺", "😞", "💗", "❤️", "🌸", "😘", "🥰"];
    let index = 0;
    function nextEmoji() {
      index = (index + 1) % emojis.length;
      document.getElementById("emoji").textContent = emojis[index];
    }

    function showPage(pageId) {
      ['home', 'game', 'message'].forEach(id => {
        document.getElementById(id).classList.add('hidden');
      });
      document.getElementById(pageId).classList.remove('hidden');
    }
  </script>
</body>
</html>
