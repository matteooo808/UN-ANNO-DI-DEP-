# UN-ANNO-DI-DEP-
Un anno di DEP, sono successe troppe cose
<!DOCTYPE html>
<html lang="it">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>UN ANNO DI DEP — 64 BARRE DI OMERTÀ</title>

<!-- OG & Meta per condivisione -->
<meta name="description" content="BrokeBoyzClub — Un anno di DEP. Partecipa al quiz per scoprire il nuovo drop.">
<meta property="og:title" content="UN ANNO DI DEP — 64 BARRE DI OMERTÀ">
<meta property="og:description" content="BrokeBoyzClub · Anniversary Drop & Exclusive Reveal">

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;700&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">

<style>
  :root{
    --bg:#07080c;
    --bg2:#0d0f16;
    --glass:rgba(255,255,255,.05);
    --glass-border:rgba(255,255,255,.1);
    --text:#eef0f6;
    --muted:#8b90a0;
    --accent:#c0c8d8;
    --accent2:#7dd3fc;
    --plat1:#f5f7fa;
    --plat2:#c9d1dc;
    --plat3:#8e99a8;
    --success:#4ade80;
    --error:#f87171;
  }
  *{margin:0;padding:0;box-sizing:border-box;}
  html,body{height:100%;}
  body{
    font-family:'Inter', sans-serif;
    background:var(--bg);
    color:var(--text);
    min-height:100vh;
    display:flex;align-items:center;justify-content:center;
    overflow-x:hidden;
    -webkit-font-smoothing:antialiased;
    user-select:none;
  }

  /* ===== CANVASES & BACKDROP ===== */
  #confettiCanvas {
    position:fixed;inset:0;width:100%;height:100%;
    z-index:90;pointer-events:none;
  }

  .backdrop{
    position:fixed;inset:0;z-index:0;
    background:
      radial-gradient(ellipse 70% 55% at 50% -10%, rgba(125,211,252,.09), transparent 60%),
      radial-gradient(ellipse 55% 45% at 85% 100%, rgba(192,200,216,.07), transparent 60%),
      linear-gradient(180deg, var(--bg) 0%, var(--bg2) 100%);
  }
  .backdrop::after{
    content:'';position:absolute;inset:0;
    background-image:
      linear-gradient(rgba(255,255,255,.025) 1px, transparent 1px),
      linear-gradient(90deg, rgba(255,255,255,.025) 1px, transparent 1px);
    background-size:64px 64px;
    mask-image:radial-gradient(ellipse 80% 70% at 50% 40%, #000 30%, transparent 75%);
    -webkit-mask-image:radial-gradient(ellipse 80% 70% at 50% 40%, #000 30%, transparent 75%);
  }
  .glow-orb{
    position:fixed;z-index:0;border-radius:50%;filter:blur(90px);opacity:.5;pointer-events:none;
  }
  .orb1{width:420px;height:420px;top:-140px;left:-120px;background:rgba(125,211,252,.12);animation:drift 14s ease-in-out infinite alternate;}
  .orb2{width:380px;height:380px;bottom:-140px;right:-100px;background:rgba(192,200,216,.1);animation:drift 18s ease-in-out infinite alternate-reverse;}
  @keyframes drift{from{transform:translate(0,0) scale(1);}to{transform:translate(50px,30px) scale(1.12);}}

  /* ===== CARD CONTAINER ===== */
  .card{
    position:relative;z-index:1;
    width:min(640px, 92vw);
    background:var(--glass);
    border:1px solid var(--glass-border);
    border-radius:28px;
    backdrop-filter:blur(20px);
    -webkit-backdrop-filter:blur(20px);
    padding:64px 44px 56px;
    margin:48px 0;
    box-shadow:0 40px 100px rgba(0,0,0,.6), inset 0 1px 0 rgba(255,255,255,.08);
    text-align:center;
  }

  /* ===== TYPOGRAPHY ===== */
  .eyebrow{
    display:inline-flex;align-items:center;gap:10px;
    font-size:.72rem;font-weight:500;letter-spacing:.28em;text-transform:uppercase;
    color:var(--muted);
    border:1px solid var(--glass-border);
    background:rgba(255,255,255,.03);
    padding:8px 18px;border-radius:100px;
    margin-bottom:34px;
  }
  .eyebrow .pulse{
    width:7px;height:7px;border-radius:50%;
    background:var(--accent2);
    box-shadow:0 0 12px var(--accent2);
    animation:pulse 2s ease-in-out infinite;
  }
  @keyframes pulse{0%,100%{opacity:1;transform:scale(1);}50%{opacity:.4;transform:scale(.75);}}

  h1.title{
    font-family:'Space Grotesk', sans-serif;
    font-weight:700;
    font-size:clamp(2.6rem, 9vw, 4.6rem);
    line-height:1.02;
    letter-spacing:-.02em;
    text-transform:uppercase;
    background:linear-gradient(135deg, #ffffff 20%, var(--plat2) 55%, var(--accent2) 110%);
    -webkit-background-clip:text;background-clip:text;
    -webkit-text-fill-color:transparent;
  }
  h1.title .line2{display:block;}
  .subtitle{
    margin-top:16px;
    color:var(--muted);
    font-size:.95rem;font-weight:300;
    letter-spacing:.02em;
  }

  /* ===== PLATINUM PLAQUE ===== */
  .plaque{
    margin:44px auto 0;
    width:min(340px, 85%);
    background:linear-gradient(165deg, rgba(255,255,255,.09), rgba(255,255,255,.02));
    border:1px solid var(--glass-border);
    border-radius:22px;
    padding:34px 26px 28px;
    position:relative;
    box-shadow:0 24px 60px rgba(0,0,0,.45), inset 0 1px 0 rgba(255,255,255,.12);
    overflow:hidden;
  }
  .plaque::before{
    content:'';position:absolute;top:0;left:0;right:0;height:60%;
    background:linear-gradient(180deg, rgba(255,255,255,.07), transparent);
    pointer-events:none;
  }
  .disc{
    width:160px;height:160px;margin:0 auto 22px;border-radius:50%;
    background:
      radial-gradient(circle at 50% 50%, var(--bg) 0 16%, transparent 16.5%),
      conic-gradient(from 200deg,
        var(--plat1) 0deg, var(--plat3) 60deg, var(--plat2) 120deg,
        var(--plat1) 180deg, var(--plat3) 240deg, var(--plat2) 300deg, var(--plat1) 360deg);
    box-shadow:
      0 12px 40px rgba(0,0,0,.55),
      0 0 0 1px rgba(255,255,255,.15),
      inset 0 0 30px rgba(255,255,255,.15);
    position:relative;
    animation:spin 9s linear infinite;
  }
  @keyframes spin{to{transform:rotate(360deg);}}
  .disc::before{
    content:'';position:absolute;inset:0;border-radius:50%;
    background:repeating-radial-gradient(circle at 50% 50%,
      transparent 0 4px, rgba(0,0,0,.12) 4px 5px);
  }
  .disc::after{
    content:'DEP';
    position:absolute;inset:0;margin:auto;
    width:52px;height:52px;border-radius:50%;
    background:linear-gradient(145deg, var(--plat1), var(--plat2));
    color:#3a4150;
    display:flex;align-items:center;justify-content:center;
    font-family:'Space Grotesk', sans-serif;
    font-weight:700;font-size:.8rem;letter-spacing:.12em;
    box-shadow:inset 0 1px 2px rgba(255,255,255,.9), 0 2px 6px rgba(0,0,0,.3);
  }
  .plaque .cert-label{
    font-size:.66rem;letter-spacing:.35em;text-transform:uppercase;
    color:var(--muted);font-weight:500;margin-bottom:8px;
  }
  .plaque .cert-name{
    font-family:'Space Grotesk', sans-serif;
    font-weight:700;
    font-size:1.9rem;letter-spacing:.04em;text-transform:uppercase;
    background:linear-gradient(120deg, var(--plat1), var(--plat2) 60%, var(--plat3));
    -webkit-background-clip:text;background-clip:text;
    -webkit-text-fill-color:transparent;
  }
  .plaque .cert-sub{
    font-size:.72rem;color:var(--muted);margin-top:10px;letter-spacing:.06em;font-weight:300;
  }

  /* ===== BUTTONS ===== */
  .btn{
    display:inline-flex;align-items:center;justify-content:center;gap:12px;
    font-family:'Space Grotesk', sans-serif;
    font-weight:700;
    font-size:1.05rem;letter-spacing:.14em;text-transform:uppercase;
    color:#0a0c12;
    background:linear-gradient(135deg, #ffffff, var(--plat2));
    border:none;cursor:pointer;
    padding:18px 40px;
    margin-top:44px;
    border-radius:100px;
    box-shadow:0 12px 40px rgba(192,200,216,.22), inset 0 1px 0 #fff;
    transition:transform .18s cubic-bezier(.34,1.56,.64,1), box-shadow .18s;
    position:relative;overflow:hidden;
    outline:none;
  }
  .btn::after{
    content:'';position:absolute;top:0;left:-80%;width:50%;height:100%;
    background:linear-gradient(105deg, transparent, rgba(255,255,255,.7), transparent);
    transform:skewX(-20deg);
    transition:left .5s ease;
  }
  .btn:hover{transform:translateY(-3px) scale(1.02);box-shadow:0 18px 55px rgba(125,211,252,.28), inset 0 1px 0 #fff;}
  .btn:hover::after{left:130%;}
  .btn:active{transform:translateY(0) scale(.98);}
  .btn:focus-visible{outline:2px solid var(--accent2);outline-offset:4px;}
  .btn .arrow{transition:transform .2s;}
  .btn:hover .arrow{transform:translateX(4px);}

  .footer-note{
    margin-top:38px;
    font-size:.66rem;letter-spacing:.3em;text-transform:uppercase;
    color:var(--muted);opacity:.7;
  }

  /* ===== SCREENS ===== */
  .screen{display:none;opacity:0;transform:translateY(20px);transition:opacity .4s ease, transform .4s ease;}
  .screen.active{display:block;opacity:1;transform:translateY(0);}

  /* ===== QUIZ SECTION ===== */
  .progress{
    display:flex;justify-content:center;align-items:center;gap:10px;margin-bottom:36px;
  }
  .progress .dot{
    width:26px;height:4px;border-radius:4px;
    background:rgba(255,255,255,.12);
    transition:background .35s, box-shadow .35s, width .35s;
  }
  .progress .dot.done{
    background:linear-gradient(90deg, var(--plat1), var(--accent2));
    box-shadow:0 0 12px rgba(125,211,252,.5);
  }
  .progress .dot.current{width:38px;background:rgba(255,255,255,.4);}

  .q-number{
    font-size:.7rem;letter-spacing:.3em;text-transform:uppercase;
    color:var(--accent2);font-weight:500;margin-bottom:14px;
  }
  .q-text{
    font-family:'Space Grotesk', sans-serif;
    font-weight:700;
    font-size:clamp(1.35rem, 4.6vw, 1.9rem);
    line-height:1.25;letter-spacing:-.01em;
    margin-bottom:36px;
  }
  .answers{display:flex;flex-direction:column;gap:14px;align-items:center;}
  
  .answer{
    width:min(440px, 100%);
    display:flex;align-items:center;gap:16px;
    font-family:'Inter', sans-serif;
    font-size:.98rem;font-weight:400;
    background:rgba(255,255,255,.04);
    color:var(--text);
    border:1px solid var(--glass-border);
    border-radius:16px;
    padding:16px 22px;
    cursor:pointer;text-align:left;
    transition:border-color .2s, background .2s, transform .18s cubic-bezier(.34,1.56,.64,1), box-shadow .2s;
    outline:none;
  }
  .answer:hover{
    background:rgba(255,255,255,.08);
    border-color:rgba(125,211,252,.5);
    transform:translateY(-2px);
    box-shadow:0 10px 30px rgba(0,0,0,.4);
  }
  .answer:focus-visible{border-color:var(--accent2);outline:none;}
  .answer:active{transform:translateY(0) scale(.99);}
  
  .answer .letter{
    flex-shrink:0;
    width:32px;height:32px;border-radius:10px;
    display:flex;align-items:center;justify-content:center;
    font-family:'Space Grotesk', sans-serif;
    font-weight:700;font-size:.9rem;
    background:rgba(255,255,255,.07);
    border:1px solid var(--glass-border);
    color:var(--accent);
    transition:background .2s, color .2s, border-color .2s;
  }
  .answer:hover .letter{background:var(--accent2);color:#0a0c12;border-color:transparent;}

  /* Stati di Risposta (Success / Error visual indicator) */
  .answer.correct{
    background:rgba(74, 222, 128, 0.15) !important;
    border-color:var(--success) !important;
    box-shadow:0 0 20px rgba(74, 222, 128, 0.3) !important;
  }
  .answer.correct .letter{
    background:var(--success) !important;
    color:#052e16 !important;
  }
  .answer.wrong{
    background:rgba(248, 113, 113, 0.15) !important;
    border-color:var(--error) !important;
    animation:shake .4s ease;
  }
  .answer.wrong .letter{
    background:var(--error) !important;
    color:#450a0a !important;
  }

  /* ===== ERROR OVERLAY ===== */
  .error-overlay{
    position:fixed;inset:0;z-index:100;
    background:rgba(5,6,10,.92);
    backdrop-filter:blur(16px);
    -webkit-backdrop-filter:blur(16px);
    display:none;
    align-items:center;justify-content:center;
    flex-direction:column;
    opacity:0;
    transition:opacity .3s ease;
  }
  .error-overlay.show{display:flex;opacity:1;}
  .error-msg{
    font-family:'Space Grotesk', sans-serif;
    font-weight:700;
    font-size:clamp(1.7rem, 6vw, 3rem);
    letter-spacing:-.01em;
    text-align:center;
    padding:0 24px;
    background:linear-gradient(120deg, #ff6b6b, #ffa8a8);
    -webkit-background-clip:text;background-clip:text;
    -webkit-text-fill-color:transparent;
    animation:shake .45s cubic-bezier(.36,.07,.19,.97);
  }
  @keyframes shake{
    10%,90%{transform:translateX(-2px);}
    20%,80%{transform:translateX(4px);}
    30%,50%,70%{transform:translateX(-7px);}
    40%,60%{transform:translateX(7px);}
  }
  .error-sub{
    color:var(--muted);font-size:.85rem;font-weight:300;
    margin-top:14px;letter-spacing:.04em;
  }
  .error-overlay .btn{margin-top:38px;}

  /* ===== FINAL REVEAL ===== */
  .reveal{padding:14px 0 6px;}
  .reveal .big{
    font-family:'Space Grotesk', sans-serif;
    font-weight:700;
    font-size:clamp(2.4rem, 9vw, 4.2rem);
    line-height:1.05;letter-spacing:-.02em;
    text-transform:uppercase;
    background:linear-gradient(135deg, #ffffff 15%, var(--plat2) 55%, var(--accent2) 110%);
    -webkit-background-clip:text;background-clip:text;
    -webkit-text-fill-color:transparent;
    animation:revealPop .7s cubic-bezier(.22,1.4,.36,1) both;
  }
  @keyframes revealPop{
    0%{opacity:0;transform:scale(.85);}
    100%{opacity:1;transform:scale(1);}
  }
  .reveal .date{
    margin-top:26px;
    font-size:1.05rem;font-weight:300;color:var(--muted);letter-spacing:.04em;
  }
  .reveal .date strong{
    display:inline-block;
    font-family:'Space Grotesk', sans-serif;
    font-weight:700;font-size:1.25em;
    color:var(--text);
    border:1px solid var(--glass-border);
    background:rgba(255,255,255,.05);
    padding:6px 18px;border-radius:12px;
    margin-left:6px;
    box-shadow:0 0 30px rgba(125,211,252,.15);
  }
  .reveal .handwritten{
    display:inline-block;
    margin-top:34px;
    font-size:.85rem;color:var(--muted);font-weight:300;letter-spacing:.05em;
  }
  .reveal .badge{
    display:inline-flex;align-items:center;gap:8px;
    margin-top:22px;
    font-size:.68rem;letter-spacing:.28em;text-transform:uppercase;
    color:#7ee2a8;font-weight:500;
    border:1px solid rgba(126,226,168,.3);
    background:rgba(126,226,168,.07);
    padding:8px 18px;border-radius:100px;
  }

  @media(max-width:480px){
    .card{padding:48px 22px 44px;border-radius:22px;}
    .disc{width:130px;height:130px;}
    .disc::after{width:44px;height:44px;font-size:.7rem;}
  }
</style>
</head>
<body>

<canvas id="confettiCanvas"></canvas>

<div class="backdrop"></div>
<div class="glow-orb orb1"></div>
<div class="glow-orb orb2"></div>

<main class="card">

  <!-- ============ SCHERMATA 1: HOME ============ -->
  <section id="screen-home" class="screen active">
    <div class="eyebrow"><span class="pulse"></span> BrokeBoyzClub · Anniversary Drop</div>

    <h1 class="title">Un anno di DEP<span class="line2">— il debutto</span></h1>
    <p class="subtitle">Un anno fa cambiava tutto. Ora si riparte.</p>

    <div class="plaque">
      <div class="disc"></div>
      <div class="cert-label">Certificazione</div>
      <div class="cert-name">Disco di Platino</div>
      <div class="cert-sub">100.000 copie scaricate a tradimento</div>
    </div>

    <button class="btn" id="startBtn">Scopri il prossimo drop <span class="arrow">→</span></button>

    <p class="footer-note">BrokeBoyzClub — nessun diritto riservato</p>
  </section>

  <!-- ============ SCHERMATA 2: QUIZ ============ -->
  <section id="screen-quiz" class="screen">
    <div class="progress" id="progress"></div>
    <p class="q-number" id="qNumber"></p>
    <h2 class="q-text" id="qText"></h2>
    <div class="answers" id="answers"></div>
  </section>

  <!-- ============ SCHERMATA 3: REVEAL ============ -->
  <section id="screen-reveal" class="screen">
    <div class="reveal">
      <div class="eyebrow" style="margin-bottom:28px;"><span class="pulse"></span> Reveal ufficiale</div>
      <h2 class="big">64 barre<br>di omertà</h2>
      <p class="date">fuori l'<strong>11 dicembre 2026</strong></p>
      <div class="badge">✓ Quiz superato — sei dei nostri</div>
      <p class="handwritten">non dire niente a nessuno.</p>
    </div>
  </section>
</main>

<!-- ============ OVERLAY ERRORE ============ -->
<div class="error-overlay" id="errorOverlay">
  <p class="error-msg" id="errorMsg"></p>
  <p class="error-sub">quiz interrotto — si ricomincia da capo.</p>
  <button class="btn" id="retryBtn">Ricomincia dal 1</button>
</div>

<script>
  // ================= WEB AUDIO SYNTH (EFFETTI SONORI) =================
  class SoundFX {
    constructor() {
      this.ctx = null;
    }
    init() {
      if (!this.ctx) {
        this.ctx = new (window.AudioContext || window.webkitAudioContext)();
      }
      if (this.ctx.state === 'suspended') {
        this.ctx.resume();
      }
    }
    click() {
      this.init();
      const osc = this.ctx.createOscillator();
      const gain = this.ctx.createGain();
      osc.type = 'sine';
      osc.frequency.setValueAtTime(400, this.ctx.currentTime);
      osc.frequency.exponentialRampToValueAtTime(800, this.ctx.currentTime + 0.05);
      gain.gain.setValueAtTime(0.1, this.ctx.currentTime);
      gain.gain.exponentialRampToValueAtTime(0.01, this.ctx.currentTime + 0.05);
      osc.connect(gain); gain.connect(this.ctx.destination);
      osc.start(); osc.stop(this.ctx.currentTime + 0.05);
    }
    correct() {
      this.init();
      const now = this.ctx.currentTime;
      const osc = this.ctx.createOscillator();
      const gain = this.ctx.createGain();
      osc.type = 'triangle';
      osc.frequency.setValueAtTime(523.25, now); // C5
      osc.frequency.setValueAtTime(659.25, now + 0.08); // E5
      gain.gain.setValueAtTime(0.15, now);
      gain.gain.exponentialRampToValueAtTime(0.01, now + 0.25);
      osc.connect(gain); gain.connect(this.ctx.destination);
      osc.start(); osc.stop(now + 0.25);
    }
    error() {
      this.init();
      const now = this.ctx.currentTime;
      const osc = this.ctx.createOscillator();
      const gain = this.ctx.createGain();
      osc.type = 'sawtooth';
      osc.frequency.setValueAtTime(160, now);
      osc.frequency.linearRampToValueAtTime(110, now + 0.25);
      gain.gain.setValueAtTime(0.2, now);
      gain.gain.exponentialRampToValueAtTime(0.01, now + 0.25);
      osc.connect(gain); gain.connect(this.ctx.destination);
      osc.start(); osc.stop(now + 0.25);
    }
    win() {
      this.init();
      const notes = [523.25, 659.25, 783.99, 1046.50]; // C5, E5, G5, C6
      notes.forEach((freq, idx) => {
        const osc = this.ctx.createOscillator();
        const gain = this.ctx.createGain();
        const now = this.ctx.currentTime + (idx * 0.1);
        osc.type = 'sine';
        osc.frequency.setValueAtTime(freq, now);
        gain.gain.setValueAtTime(0.15, now);
        gain.gain.exponentialRampToValueAtTime(0.001, now + 0.4);
        osc.connect(gain); gain.connect(this.ctx.destination);
        osc.start(now); osc.stop(now + 0.4);
      });
    }
  }
  const sfx = new SoundFX();

  // ================= DATI DOMANDE ED ERRORI =================
  const questions = [
    {
      q: "Quando è uscito originariamente DEP?",
      answers: ["9 settembre", "7 settembre", "7 luglio"],
      correct: 0
    },
    {
      q: "Quante tracce ha DEP su SoundCloud?",
      answers: ["14", "15", "16"],
      correct: 0
    },
    {
      q: "Perché Marco Mazzoli non si trova più sulle piattaforme di streaming?",
      answers: ["Perché non gli piaceva.", "Perché hanno preferito così.", "Per colpa di una denuncia."],
      correct: 2
    },
    {
      q: "Quale delle canzoni elencate ha sostituito una canzone che è presente solamente su SoundCloud?",
      answers: ["semper", "no vabbà", "Ti consiglio"],
      correct: 1
    },
    {
      q: "Qual è la prima canzone ad essere registrata dai BrokeBoyzClub?",
      answers: ["Dibala", "Semper", "Scout"],
      correct: 0
    },
    {
      q: "Come si doveva chiamare in origine DEP?",
      answers: ["Sberla 666", "ICS", "ma anche no"],
      correct: 1
    }
  ];

  const errorMessages = [
    "meglio che esci dal sito",
    "vai a fare in culo",
    "ma lo hai mai sentito l'album?",
    "per forza sei parente a Tommaso",
    "ma mica sei palestinese"
  ];

  let currentQ = 0;
  let errorIndex = 0;
  let isAnswering = false;

  const screens = {
    home: document.getElementById('screen-home'),
    quiz: document.getElementById('screen-quiz'),
    reveal: document.getElementById('screen-reveal')
  };

  // ================= CAMBIO SCHERMATA =================
  function showScreen(name){
    Object.values(screens).forEach(s => {
      s.classList.remove('active');
    });
    setTimeout(() => {
      screens[name].classList.add('active');
    }, 50);
  }

  function renderProgress(){
    const prog = document.getElementById('progress');
    prog.innerHTML = '';
    questions.forEach((_, i) => {
      const dot = document.createElement('div');
      let cls = 'dot';
      if (i < currentQ) cls += ' done';
      else if (i === currentQ) cls += ' current';
      dot.className = cls;
      prog.appendChild(dot);
    });
  }

  function renderQuestion(){
    isAnswering = false;
    const q = questions[currentQ];
    document.getElementById('qNumber').textContent = `domanda ${currentQ + 1} di ${questions.length}`;
    document.getElementById('qText').textContent = q.q;

    const letters = ['A', 'B', 'C'];
    const box = document.getElementById('answers');
    box.innerHTML = '';
    
    q.answers.forEach((ans, i) => {
      const btn = document.createElement('button');
      btn.className = 'answer';
      btn.dataset.index = i;
      btn.innerHTML = `<span class="letter">${letters[i]}</span><span>${ans}</span>`;
      btn.addEventListener('click', () => handleAnswerSelect(i, btn));
      box.appendChild(btn);
    });
    renderProgress();
  }

  function handleAnswerSelect(i, btnElement){
    if (isAnswering) return;
    isAnswering = true;

    if (i === questions[currentQ].correct){
      sfx.correct();
      btnElement.classList.add('correct');
      currentQ++;
      
      setTimeout(() => {
        if (currentQ >= questions.length){
          sfx.win();
          showScreen('reveal');
          launchConfetti();
        } else {
          renderQuestion();
        }
      }, 450);

    } else {
      sfx.error();
      btnElement.classList.add('wrong');
      
      setTimeout(() => {
        const overlay = document.getElementById('errorOverlay');
        const msg = document.getElementById('errorMsg');
        msg.textContent = errorMessages[errorIndex];
        errorIndex = (errorIndex + 1) % errorMessages.length;
        overlay.classList.add('show');
      }, 500);
    }
  }

  function restartQuiz(){
    sfx.click();
    currentQ = 0;
    const overlay = document.getElementById('errorOverlay');
    overlay.classList.remove('show');
    showScreen('quiz');
    renderQuestion();
  }

  // Event Listener Pulsanti Principali
  document.getElementById('startBtn').addEventListener('click', () => {
    sfx.click();
    currentQ = 0;
    showScreen('quiz');
    renderQuestion();
  });

  document.getElementById('retryBtn').addEventListener('click', restartQuiz);

  // ================= SCORCIATOIE DA TASTIERA =================
  document.addEventListener('keydown', (e) => {
    const key = e.key.toLowerCase();
    
    // Gestione risposte con A, B, C o 1, 2, 3
    if (screens.quiz.classList.contains('active') && !isAnswering) {
      const keyMap = { 'a': 0, '1': 0, 'b': 1, '2': 1, 'c': 2, '3': 2 };
      if (keyMap[key] !== undefined) {
        const buttons = document.querySelectorAll('.answers .answer');
        if (buttons[keyMap[key]]) {
          buttons[keyMap[key]].click();
        }
      }
    }
    
    // Enter / Space per Start e Restart
    if (key === 'enter' || key === ' ') {
      if (document.getElementById('errorOverlay').classList.contains('show')) {
        restartQuiz();
      } else if (screens.home.classList.contains('active')) {
        document.getElementById('startBtn').click();
      }
    }
  });

  // ================= CORIANDOLI CANVAS =================
  function launchConfetti() {
    const canvas = document.getElementById('confettiCanvas');
    const ctx = canvas.getContext('2d');
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;

    const pieces = [];
    const colors = ['#f5f7fa', '#c9d1dc', '#7dd3fc', '#ffffff', '#38bdf8'];

    for (let i = 0; i < 90; i++) {
      pieces.push({
        x: Math.random() * canvas.width,
        y: Math.random() * canvas.height - canvas.height,
        size: Math.random() * 8 + 4,
        color: colors[Math.floor(Math.random() * colors.length)],
        speedY: Math.random() * 3 + 2,
        speedX: Math.random() * 2 - 1,
        rotation: Math.random() * 360,
        rotSpeed: Math.random() * 4 - 2
      });
    }

    let animationFrame;
    function render() {
      ctx.clearRect(0, 0, canvas.width, canvas.height);
      let active = false;

      pieces.forEach(p => {
        p.y += p.speedY;
        p.x += p.speedX;
        p.rotation += p.rotSpeed;

        if (p.y < canvas.height) active = true;

        ctx.save();
        ctx.translate(p.x, p.y);
        ctx.rotate((p.rotation * Math.PI) / 180);
        ctx.fillStyle = p.color;
        ctx.fillRect(-p.size / 2, -p.size / 2, p.size, p.size);
        ctx.restore();
      });

      if (active) {
        animationFrame = requestAnimationFrame(render);
      } else {
        ctx.clearRect(0, 0, canvas.width, canvas.height);
      }
    }
    render();
  }

  // Resize canvas on screen resize
  window.addEventListener('resize', () => {
    const canvas = document.getElementById('confettiCanvas');
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;
  });
</script>
</body>
</html>
