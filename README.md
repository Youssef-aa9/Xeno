# Xeno
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Xeno</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <h1>Xeno</h1>
  <div id="game">
    <p>Ressource commune : <span id="common">0</span></p>
    <p>Ressource rare : <span id="rare">0</span></p>
    <button onclick="farm()">Farmer</button>
    <button onclick="tryFindRare()">Tenter de trouver une ressource rare</button>
  </div>
  <script src="script.js"></script>
</body>
</html>
body {
  font-family: Arial, sans-serif;
  text-align: center;
  padding: 30px;
  background-color: #f4f4f4;
}

#game {
  background: white;
  padding: 20px;
  display: inline-block;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0,0,0,0.1);
}

button {
  margin: 10px;
  padding: 10px 20px;
  font-size: 16px;
}
let common = 0;
let rare = 0;

function farm() {
  common++;
  document.getElementById("common").textContent = common;
}

function tryFindRare() {
  const chance = Math.random();
  if (chance < 0.1) { // 10% de chance
    rare++;
    alert("Tu as trouvé une ressource rare !");
  } else {
    alert("Rien trouvé cette fois...");
  }
  document.getElementById("rare").textContent = rare;
}
