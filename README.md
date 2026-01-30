<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>200 motivos pra te amar, Rafaella 💖</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

<style>
*{
  box-sizing:border-box;
  -webkit-tap-highlight-color:transparent;
}

body{
  margin:0;
  font-family:'Poppins',sans-serif;
  background:linear-gradient(135deg,#ff758c,#ff7eb3,#fad0c4);
  color:#fff;
  overflow-x:hidden;
}

header{
  text-align:center;
  padding:45px 20px 25px;
  animation:fadeDown 1.2s ease;
}

header h1{
  font-family:'Great Vibes',cursive;
  font-size:3rem;
  margin:0;
}

header p{
  margin-top:12px;
  font-size:1rem;
  opacity:.95;
}

.container{
  max-width:820px;
  margin:auto;
  padding:15px;
}

.card{
  background:rgba(255,255,255,.2);
  backdrop-filter:blur(14px);
  border-radius:26px;
  padding:22px;
  margin-bottom:20px;
  box-shadow:0 15px 30px rgba(0,0,0,.25);
  animation:fadeUp 1s ease;
}

.contador{
  text-align:center;
  font-size:1.15rem;
}

button{
  background:linear-gradient(135deg,#ff4f81,#ff6fa5);
  border:none;
  padding:14px 28px;
  border-radius:40px;
  color:white;
  font-size:1rem;
  cursor:pointer;
  margin-top:18px;
  box-shadow:0 8px 18px rgba(0,0,0,.25);
  animation:pulse 2s infinite;
}

.motivo{
  padding:10px 0;
  border-bottom:1px solid rgba(255,255,255,.3);
  font-size:.95rem;
  animation:fadeIn .7s ease forwards;
}

.motivo:last-child{
  border-bottom:none;
}

footer{
  text-align:center;
  padding:30px 15px;
  font-size:.9rem;
  opacity:.9;
}

.music-btn{
  position:fixed;
  top:15px;
  right:15px;
  background:rgba(255,255,255,.35);
  border-radius:50%;
  width:50px;
  height:50px;
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:22px;
  cursor:pointer;
  z-index:10;
  animation:pulse 2s infinite;
}

.heart{
  position:fixed;
  bottom:-20px;
  font-size:22px;
  animation:floatUp linear infinite;
  opacity:.85;
}

@keyframes floatUp{
  from{transform:translateY(0) scale(1);opacity:1;}
  to{transform:translateY(-120vh) scale(1.6);opacity:0;}
}
@keyframes fadeUp{
  from{opacity:0;transform:translateY(30px);}
  to{opacity:1;transform:translateY(0);}
}
@keyframes fadeDown{
  from{opacity:0;transform:translateY(-30px);}
  to{opacity:1;transform:translateY(0);}
}
@keyframes fadeIn{
  from{opacity:0;}
  to{opacity:1;}
}
@keyframes pulse{
  0%{transform:scale(1);}
  50%{transform:scale(1.05);}
  100%{transform:scale(1);}
}
.foto-amor{
  width:140px;
  height:140px;
  margin:20px auto 0;
  border-radius:50%;
  overflow:hidden;
  box-shadow:0 10px 25px rgba(0,0,0,.25);
  border:4px solid rgba(255,255,255,.6);
}

.foto-amor img{
  width:100%;
  height:100%;
  object-fit:cover;
}

</style>
</head>

<body>

<audio id="musica" loop>
  <source src="musica.mp3" type="audio/mpeg">
</audio>

<div class="music-btn" onclick="toggleMusic()">🎶</div>

<header>
  <h1>Rafaella 💕</h1>
  <p>200 motivos pra eu te amar… e mesmo assim ainda faltam palavras.</p>

  <div class="foto-amor">
    <img src="IMG_7799.jpg" alt="Nós dois 💖">
  </div>
</header>

<div class="container">
  <div class="card contador">
    💖 <span id="contador">0</span> motivos  
    <br>que moram no meu coração.
    <br>
    <button onclick="mostrarMotivos()">Começar 💌</button>
  </div>

  <div class="card" id="lista"></div>
</div>

<footer>
  Feito com todo meu amor 🤍
</footer>

<script>
const motivos = [
"seu sorriso","seus olhos","seus cabelos","seu jeito","seu coração",
"seu toque","sua presença","sua voz","sua lealdade","seu brilho",
"sua calma","sua gentileza","seu amor","seu foco","seu otimismo",
"sua resiliência","sua ternura","sua compaixão","sua bondade","sua força",
"seu carinho","seu encanto","seu estilo","sua energia","seu sorriso",
"sua luz","sua coragem","seu humor","seu jeito","sua alma",
"seu brilho","sua graça","sua sensibilidade","sua sinceridade","seu afeto",
"sua honestidade","seu apoio","sua dedicação","sua paciência","seu amor",
"seu cuidado","seu calor","sua suavidade","seu charme","sua imaginação",
"sua sinceridade","sua lealdade","seu espírito","sua felicidade","sua inteligência",
"sua generosidade","seu entendimento","sua serenidade","sua perseverança","seu ritmo",
"sua doçura","sua confiança","sua paz","seu olhar","seu abraço",
"seu vínculo","seu carinho","sua liberdade","sua fé","sua compreensão",
"sua tranquilidade","seu equilíbrio","sua vitalidade","sua empatia","sua alegria",
"sua inteligência","sua esperança","seu aconchego","sua suavidade","sua generosidade",
"seu altruismo","seu apoio","sua bondade","seu coração","sua sinceridade",
"seu humor","sua criatividade","sua empatia","sua espontaneidade","seu olhar",
"sua autenticidade","sua harmonia","sua honestidade","seu entusiasmo","sua determinação",
"sua tranquilidade","sua independência","sua risada","sua preocupação","sua alegria",
"sua positividade","sua amizade","sua proteção","sua admiração","sua visão",
"seu otimismo","seu respeito","sua beleza","sua espontaneidade","seu consolo",
"sua ternura","sua humildade","seu espírito","seu vigor","seu respeito",
"sua sinceridade","sua calma","sua gratidão","seu cuidado","sua generosidade",
"sua energia","seu encantamento","sua perspicácia","sua empatia","sua gratidão",
"seu entusiasmo","sua suavidade","seu acolhimento","sua confiança","sua dedicação",
"sua inteligência","sua coragem","sua paz","sua fortaleza","seu zelo",
"sua ternura","sua paciência","sua entrega","sua compaixão","sua presença",
"seu foco","sua resiliência","sua sensatez","seu amor","sua amizade",
"sua força","sua gentileza","sua paixão","seu charme","sua serenidade",
"sua positividade","seu apoio","sua estabilidade","seu apoio","seu calor",
"sua atenção","sua serenidade","sua leveza","sua alegria","seu orgulho",
"sua persistência","seu carinho","sua sabedoria","seu espírito","sua confiança",
"sua autenticidade","sua tranquilidade","seu amor","sua sinceridade","seu encanto",
"sua tenacidade","sua adaptação","sua verdade","sua beleza","seu alívio",
"seu afeto","sua bondade","seu magnetismo","sua visão","sua sabedoria",
"seu humor","sua calma","sua criatividade","seu olhar","sua resiliência",
"sua alegria","seu empenho","sua suavidade","sua sinceridade","seu brilho",
"sua fé","sua força","seu apoio","sua espiritualidade","sua confiança",
"sua dedicação","seu afeto","sua felicidade","sua energia","sua habilidade",
"sua generosidade","sua sabedoria","seu zelo","sua luz","você inteira"
];

let index = 0;
let tocando = false;

function mostrarMotivos(){
  const lista = document.getElementById("lista");
  const contador = document.getElementById("contador");

  const intervalo = setInterval(()=>{
    if(index >= motivos.length){
      clearInterval(intervalo);
      explosaoDeCoracoes();
      return;
    }

    const div = document.createElement("div");
    div.className="motivo";
    div.innerHTML=`💖 <strong>${index+1}.</strong> ${motivos[index]}`;
    lista.appendChild(div);

    contador.textContent=index+1;
    criarCoracao();
    index++;
  },120);
}

function criarCoracao(){
  const heart=document.createElement("div");
  heart.className="heart";
  heart.innerHTML="💗";
  heart.style.left=Math.random()*100+"vw";
  heart.style.animationDuration=(3+Math.random()*3)+"s";
  document.body.appendChild(heart);
  setTimeout(()=>heart.remove(),6000);
}

function explosaoDeCoracoes(){
  for(let i=0;i<100;i++){
    const heart=document.createElement("div");
    heart.className="heart";
    heart.innerHTML=["💖","💗","💘","💕"][Math.floor(Math.random()*4)];
    heart.style.left=Math.random()*100+"vw";
    heart.style.fontSize=(18+Math.random()*25)+"px";
    heart.style.animationDuration=(2+Math.random()*2)+"s";
    document.body.appendChild(heart);
    setTimeout(()=>heart.remove(),5000);
  }
}

function toggleMusic(){
  const musica=document.getElementById("musica");
  tocando ? musica.pause() : musica.play();
  tocando=!tocando;
}
</script>

</body>
</html>>
