# cartao-L-via
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>Feliz Aniversário, Lívia 💖</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
:root {
  --bg1: #ff9a9e;
  --bg2: #fad0c4;
  --card: #ffffff;
  --text: #555;
  --title: #ff4d6d;
}

body.dark {
  --bg1: #1e1e2f;
  --bg2: #2b2b40;
  --card: #2f2f44;
  --text: #ddd;
  --title: #ff8fab;
}

body {
  margin: 0;
  min-height: 100vh;
  font-family: Arial, sans-serif;
  background: linear-gradient(135deg, var(--bg1), var(--bg2));
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px;
  overflow: hidden;
}

.card {
  background: var(--card);
  max-width: 500px;
  padding: 30px;
  border-radius: 22px;
  box-shadow: 0 15px 35px rgba(0,0,0,0.25);
  text-align: center;
  display: none;
  animation: fadeIn 1.2s ease forwards;
  z-index: 2;
}

h1 {
  color: var(--title);
  margin-bottom: 20px;
}

p {
  color: var(--text);
  font-size: 1.05em;
  line-height: 1.7;
  text-align: left;
}

footer {
  margin-top: 25px;
  text-align: right;
  color: var(--text);
}

button {
  padding: 14px 26px;
  font-size: 1.1em;
  border: none;
  border-radius: 30px;
  cursor: pointer;
  background: #ff4d6d;
  color: white;
  box-shadow: 0 8px 20px rgba(0,0,0,0.2);
}

.toggle {
  position: fixed;
  top: 15px;
  right: 15px;
  font-size: 0.9em;
  padding: 10px 16px;
}

.start {
  z-index: 2;
}

iframe {
  width: 100%;
  height: 80px;
  border-radius: 12px;
  margin-top: 15px;
}

@keyframes fadeIn {
  from {opacity: 0; transform: translateY(25px);}
  to {opacity: 1; transform: translateY(0);}
}

/* CONFETES */
.confetti {
  position: fixed;
  top: -10px;
  width: 10px;
  height: 10px;
  background: red;
  animation: fall linear infinite;
}

@keyframes fall {
  to {
    transform: translateY(110vh) rotate(360deg);
  }
}
</style>
</head>

<body>

<button class="toggle" onclick="toggleDark()">🌙 Modo</button>

<div class="start">
  <button onclick="startCard()">💌 Clique para ler</button>
</div>

<div class="card" id="card">
  <h1>Feliz Aniversário, Lívia! 🎉</h1>

  <p>
    Feliz aniversário Lívia, que vc seja muito feliz e que aproveite cada minuto da sua vida,
    pq vc é uma pessoa incrível (sério, nao entendo como vc é tããão incrível).
  </p>

  <p>
    Tmb queria agradecer por cada momento bom q vc ja me proporcionou com a sua companhia,
    tanto presente quanto online, momentos q eu guardo na minha memória com muito carinho,
    vc me vendo jogar vôlei, nossos bullyngs, a gente fofocando sobre relacionamento dos outros,
    eu te vendo zerar tlou 2 (foi ali q eu cmc a me apaixonar),
    aquele dia q vc tava tirando meus cravos (tmb foi um dia q eu nunca esqueci),
    a gente zoando o Pedro por vc sabe oq... o xoso trabalhando de pombo correio nosso pra gente conversar,
    nosso mapa do mine (a gente precisa jogar, ja to com abstinência).
  </p>

  <p>
    E diversos outros momentos e coisas incrível q eu descobri com vc (tipo o link do zap),
    todos esses momentos eu guardo num cantinho especial do meu coração,
    e espero q tenhamos mais momentos juntos ❤️
  </p>

  <iframe src="https://open.spotify.com/embed/track/3cbU5Xteq2JcHVJ8uT6XGo?utm_source=generator"
    allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture">
  </iframe>

  <footer>
    — Com amor: <strong>Manolo</strong>
  </footer>
</div>

<script>
function startCard() {
  document.querySelector('.start').style.display = 'none';
  document.getElementById('card').style.display = 'block';
  startConfetti();
}

function toggleDark() {
  document.body.classList.toggle('dark');
}

function startConfetti() {
  for (let i = 0; i < 120; i++) {
    const confetti = document.createElement('div');
    confetti.className = 'confetti';
    confetti.style.left = Math.random() * 100 + 'vw';
    confetti.style.background = `hsl(${Math.random()*360},100%,60%)`;
    confetti.style.animationDuration = (Math.random() * 3 + 2) + 's';
    confetti.style.opacity = Math.random();
    document.body.appendChild(confetti);
  }
}
</script>

</body>
</html>
