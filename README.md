<!DOCTYPE html>
<html lang="ms">
<head>
<meta charset="UTF-8">
<title>Selamat Hari Guru</title>

<!-- 💙 FONT Poppins -->
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;800&display=swap" rel="stylesheet">

<style>
body {
  margin: 0;
  height: 100vh;
  overflow: hidden;
  font-family: 'Poppins', sans-serif;
  background: linear-gradient(to top, #001219, #003049, #005f73);
}

/* 🌊 TITLE GLASS + GLOW */
h1 {
  position: absolute;
  top: 22%;
  width: 100%;
  text-align: center;
  font-size: 45px;
  font-weight: 800;

  background: linear-gradient(90deg, #ffffff, #7bdff2, #ccefff, #ffffff);
  background-size: 300% 300%;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;

  animation: gradientMove 5s infinite linear, fadeIn 2s ease-in-out;
  text-shadow: 0 0 20px rgba(123, 223, 242, 0.5);
}

@keyframes gradientMove {
  0% {background-position: 0%;}
  100% {background-position: 300%;}
}

/* 💌 MESSAGE */
.message {
  position: absolute;
  top: 38%;
  width: 100%;
  text-align: center;
  color: #d0f0ff;
  font-size: 18px;
  animation: fadeIn 4s ease-in-out;
}

/* 🪷 TRIBUTE TEXT */
.tribute {
  position: absolute;
  top: 50%;
  width: 100%;
  text-align: center;
  color: white;
  font-size: 20px;
  padding: 0 20px;
  line-height: 1.6;
  animation: fadeIn 6s ease-in-out;
  text-shadow: 0 0 10px rgba(255,255,255,0.3);
}

@keyframes fadeIn {
  from {opacity: 0; transform: translateY(20px);}
  to {opacity: 1; transform: translateY(0);}
}

/* 🌊 WAVES */
.wave {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 200%;
  height: 120px;
  background: rgba(255,255,255,0.15);
  border-radius: 1000px 1000px 0 0;
  animation: waveMove 8s linear infinite;
}

.wave:nth-child(2) {
  bottom: 10px;
  opacity: 0.4;
  animation: waveMove 12s linear infinite reverse;
}

.wave:nth-child(3) {
  bottom: 20px;
  opacity: 0.2;
  animation: waveMove 15s linear infinite;
}

@keyframes waveMove {
  0% {transform: translateX(0);}
  100% {transform: translateX(-50%);}
}

/* 🪷 FLOATING GARDEN */
.float {
  position: absolute;
  bottom: -80px;
  font-size: 30px;
  animation: rise linear infinite;
  filter: drop-shadow(0 0 10px rgba(255,255,255,0.4));
}

@keyframes rise {
  0% {transform: translateY(0) rotate(0deg); opacity: 0;}
  20% {opacity: 1;}
  100% {transform: translateY(-120vh) rotate(360deg); opacity: 0;}
}

/* ✨ glow particles */
.glow {
  position: absolute;
  bottom: -50px;
  width: 8px;
  height: 8px;
  background: rgba(255,255,255,0.5);
  border-radius: 50%;
  animation: floatGlow 10s linear infinite;
}

@keyframes floatGlow {
  from {transform: translateY(0); opacity: 0;}
  to {transform: translateY(-120vh); opacity: 1;}
}
</style>
</head>

<body>

<!-- 🎶 MUSIC (letak file music.mp3) -->
<audio autoplay loop controls>
  <source src="music.mp3" type="audio/mpeg">
</audio>

<!-- 💙 TEXT -->
<h1>Selamat Hari Guru 💙</h1>

<div class="message">
Terima kasih cikgu atas segala ilmu & pengorbanan 🫶
</div>

<div class="tribute">
Selamat hari guru cikgu bashirah 🪷<br>
kami sayangg cikguu 💙 semoga cikgu bahagia<br>
dan sentiasa bersabar dengan 4ALF 🩵
</div>

<!-- 🌊 WAVES -->
<div class="wave"></div>
<div class="wave"></div>
<div class="wave"></div>

<script>
const items = ["🪷", "🌸", "🌺", "💙", "🌿"];

/* floating garden */
function createFloat() {
  const el = document.createElement("div");
  el.className = "float";
  el.innerHTML = items[Math.floor(Math.random() * items.length)];

  el.style.left = Math.random() * window.innerWidth + "px";
  el.style.fontSize = (20 + Math.random() * 35) + "px";
  el.style.animationDuration = (5 + Math.random() * 7) + "s";

  document.body.appendChild(el);
  setTimeout(() => el.remove(), 12000);
}
setInterval(createFloat, 200);

/* glow particles */
function glow() {
  const g = document.createElement("div");
  g.className = "glow";

  g.style.left = Math.random() * window.innerWidth + "px";
  g.style.animationDuration = (6 + Math.random() * 5) + "s";

  document.body.appendChild(g);
  setTimeout(() => g.remove(), 12000);
}
setInterval(glow, 150);
</script>

</body>
</html>
