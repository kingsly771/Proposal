<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Pour toi, ma princesse 💖</title>

<style>
  body{
    margin:0;
    font-family:"Poppins",Arial,sans-serif;
    background: radial-gradient(#1b0033,#2b0c59,#7b2cbf);
    color:#fff;text-align:center;
    overflow-y:auto;overflow-x:hidden;
  }

  header{padding:28px 10px;}
  h1{margin:0;font-size:28px;}
  .subtitle{opacity:.9;margin-top:6px;}

  .gold-ribbon{
    margin:10px auto 15px;
    display:inline-block;padding:10px 18px;
    border-radius:30px;
    background:linear-gradient(120deg,#ffd27f,#ffbf3c,#ffda96);
    color:#442200;font-weight:600;
  }

  /* 🎁 Cartes surprise — flip 3D */
  .carousel{
    display:flex;gap:12px;
    overflow-x:auto;padding:15px;
    scroll-behavior:smooth;
  }

  .card{
    min-width:260px;height:180px;
    perspective:900px;
    position:relative;
  }

  .inner{
    width:100%;height:100%;
    border-radius:18px;
    position:relative;
    transform-style:preserve-3d;
    transition:transform .6s;
    box-shadow:0 0 20px rgba(255,170,255,.35);
    cursor:pointer;
  }

  .card.flipped .inner{
    transform:rotateY(180deg);
  }

  /* 💎 ✨ ÉCLAT DORÉ SPÉCIAL */
  .card::after{
    content:"";
    position:absolute;
    inset:-6px;
    border-radius:22px;
    background:conic-gradient(
      from 0deg,
      rgba(255,215,120,0) 0%,
      rgba(255,220,140,.9) 20%,
      rgba(255,240,190,.6) 35%,
      rgba(255,215,120,.9) 55%,
      rgba(255,215,120,0) 70%
    );
    opacity:0;
    filter:blur(4px);
    transition:.4s;
    pointer-events:none;
  }

  .card.flipped::after{
    opacity:1;
    animation:goldPulse 1.3s ease-out forwards;
  }

  @keyframes goldPulse{
    0%{transform:scale(.9);opacity:.6;}
    40%{transform:scale(1.08);opacity:1;}
    100%{transform:scale(1);opacity:.8;}
  }

  .face{
    position:absolute;inset:0;
    display:flex;align-items:center;justify-content:center;
    padding:14px;line-height:1.6;
    border-radius:18px;
    backface-visibility:hidden;
    border:1px solid rgba(255,200,255,.4);
  }
  .front{background:rgba(0,0,0,.55);}
  .back{
    background:linear-gradient(135deg,#ff6fb0,#ff92c8);
    transform:rotateY(180deg);
  }

  /* 💌 Poème */
  .poem-box{
    max-width:900px;margin:25px auto 30px;
    padding:22px;border-radius:18px;
    background:rgba(0,0,0,.55);
    line-height:1.8;
  }

  .surprise-btn{
    margin-top:12px;background:#ff69b4;border:none;
    color:#fff;padding:12px 22px;border-radius:30px;
  }

  .final-message{
    position:fixed;inset:0;background:rgba(0,0,0,.92);
    display:flex;align-items:center;justify-content:center;
    text-align:center;padding:20px;font-size:24px;
    opacity:0;pointer-events:none;transition:.5s;
  }
  .final-message.show{opacity:1;pointer-events:auto;}

  /* ✨ Effets spéciaux */
  .tap-heart{
    position:fixed;
    font-size:18px;
    pointer-events:none;
    animation:rise 1.2s ease-out forwards;
  }
  @keyframes rise{
    from{transform:translateY(0) scale(1);opacity:1;}
    to{transform:translateY(-80px) scale(1.8);opacity:0;}
  }

  .spark{
    position:fixed;
    width:8px;height:8px;
    border-radius:50%;
    background:#ffd6ff;
    pointer-events:none;
    opacity:0.9;
    animation:sparkle 1s linear forwards;
  }
  @keyframes sparkle{
    from{transform:scale(1);opacity:1;}
    to{transform:scale(2);opacity:0;}
  }
</style>
</head>

<body>

<audio id="music"
src="https://cdn.pixabay.com/download/audio/2022/02/23/audio_3c40b9.mp3?filename=romantic-piano-10328.mp3"
loop></audio>

<header>
  <h1>✨ Pour toi, ma princesse ✨</h1>
  <p class="subtitle">Parce que tu comptes plus que tout pour moi 💕</p>
</header>

<div class="gold-ribbon">
  💍 Notre promesse d’amour — <b>1 janvier 2026</b>
</div>

<!-- 🎁 CARTES SURPRISE -->
<div class="carousel" id="carousel">

  <div class="card" onclick="flip(this)">
    <div class="inner">
      <div class="face front">🌷 Tu es la plus belle chose de ma vie</div>
      <div class="face back">💖 Sans toi… mon monde ne serait pas complet</div>
    </div>
  </div>

  <div class="card" onclick="flip(this)">
    <div class="inner">
      <div class="face front">💕 Tu comptes énormément pour moi</div>
      <div class="face back">✨ Tu es ma force, mon soutien, mon espoir</div>
    </div>
  </div>

  <div class="card" onclick="flip(this)">
    <div class="inner">
      <div class="face front">❤️ Chaque jour à tes côtés est un cadeau</div>
      <div class="face back">🌹 Merci d’exister dans ma vie</div>
    </div>
  </div>

  <div class="card" onclick="flip(this)">
    <div class="inner">
      <div class="face front">💞 Tu as une place unique dans mon cœur</div>
      <div class="face back">💍 Personne ne pourra jamais la remplacer</div>
    </div>
  </div>

  <div class="card" onclick="flip(this)">
    <div class="inner">
      <div class="face front">✨ Avec toi, tout prend un sens</div>
      <div class="face back">🤍 Tu es mon présent… et mon avenir</div>
    </div>
  </div>

  <div class="card" onclick="flip(this)">
    <div class="inner">
      <div class="face front">🌹 Ta présence rend mes jours plus doux</div>
      <div class="face back">💗 Tu es mon bb, ma princesse, ma vie</div>
    </div>
  </div>

  <div class="card" onclick="flip(this)">
    <div class="inner">
      <div class="face front">💍 Avec toi, je ne vois plus un rêve</div>
      <div class="face back">✨ Je vois <b>nos espoirs</b> devenir réalité</div>
    </div>
  </div>

  <div class="card" onclick="flip(this)">
    <div class="inner">
      <div class="face front">💖 Tu comptes plus que tout pour moi</div>
      <div class="face back">🥹 Et je veux prendre soin de toi… pour toujours</div>
    </div>
  </div>

</div>

<!-- 💍 POÈME -->
<div class="poem-box">
  <h2>💍 Ma princesse… j’ai quelque chose à te dire</h2>
  <p>
    Depuis le jour où nos chemins se sont croisés,<br>
    mon cœur a trouvé un endroit où il peut enfin se reposer.<br>
    Avec toi, la vie est plus douce, plus belle, plus vraie,<br>
    et chaque instant à tes côtés est un cadeau que je chéris profondément.<br><br>

    Même si notre histoire s’est construite à distance,<br>
    jamais je ne l’ai vue comme quelque chose d’irréel.<br>
    Parce que dans ta voix, j’ai trouvé de la tendresse,<br>
    dans ton sourire, j’ai trouvé la lumière,<br>
    dans ton amour, j’ai trouvé la vérité,<br>
    et dans ta passion… j’ai senti la force de notre lien.<br><br>

    Chaque fois que j’entends ta voix, mon cœur se rassure,<br>
    chaque fois que j’imagine ton sourire, le monde devient plus beau.<br>
    Et même loin de moi, je sens ton amour près du mien,<br>
    comme si nos âmes s’étaient reconnues avant même de se toucher.<br><br>

    Mon bb, tu comptes plus que tout pour moi.<br>
    Ta voix apaise mon âme, ton sourire illumine mes jours,<br>
    ton amour me fait grandir, et ta passion donne vie à mes rêves.<br><br>

    Ma vie, je veux marcher avec toi — dans le réel comme dans nos rêves —,<br>
    protéger ton cœur, respecter ton âme,<br>
    t’aimer aujourd’hui, demain… et pour toujours.<br><br>

    Alors aujourd’hui, avec tout l’amour que je porte en moi,<br>
    devant notre histoire, nos promesses, notre avenir…<br><br>

    <b>Ma princesse… accepterais-tu de continuer ce chemin à mes côtés<br>
    et de devenir ma femme ? 💍💖</b>
  </p>

  <button class="surprise-btn" onclick="sayYes()">❤️ Oui, je dis oui</button>
</div>

<div class="final-message" id="finalMsg">
  💖 Merci, ma princesse…<br>
  Notre histoire devient notre promesse pour toujours 💍✨<br><br>
  <small>🌹 Date de notre engagement : <b>1 janvier 2026</b></small><br><br>
  <i>Pour toujours… ton bb, ton cœur, ta vie 💞</i>
</div>

<script>
const music=document.getElementById("music");
let musicStarted=false;
function startMusic(){ if(!musicStarted){ music.play().catch(()=>{}); musicStarted=true; } }

function flip(card){
  startMusic();
  card.classList.toggle("flipped");
}

function sayYes(){
  startMusic();
  document.getElementById("finalMsg").classList.add("show");
}

/* 🌸 Défilement automatique */
const carousel=document.getElementById("carousel");
let autoScroll=setInterval(()=>{
  carousel.scrollBy({left:280,behavior:"smooth"});
  if(carousel.scrollLeft+carousel.clientWidth>=carousel.scrollWidth-5){
    setTimeout(()=>carousel.scrollTo({left:0,behavior:"smooth"}),800);
  }
},3000);
carousel.addEventListener("touchstart",()=>clearInterval(autoScroll));
carousel.addEventListener("mousedown",()=>clearInterval(autoScroll));

/* ❤️ Effets au tap */
document.addEventListener("click", e=>{
  startMusic();
  for(let i=0;i<4;i++){
    const h=document.createElement("div");
    h.className="tap-heart";
    h.textContent="❤";
    h.style.left=(e.clientX+Math.random()*20-10)+"px";
    h.style.top =(e.clientY+Math.random()*20-10)+"px";
    document.body.appendChild(h);
    setTimeout(()=>h.remove(),1200);
  }
});

/* ✨ Étincelles lors du scroll */
window.addEventListener("scroll", ()=>{
  const s=document.createElement("div");
  s.className="spark";
  s.style.left=(Math.random()*100)+"vw";
  s.style.top=(Math.random()*100)+"vh";
  document.body.appendChild(s);
  setTimeout(()=>s.remove(),1000);
});
</script>

</body>
</html>
