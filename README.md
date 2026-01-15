[Index (1).html](https://github.com/user-attachments/files/24631247/Index.1.html)
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Okta ❤ Eva</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&family=Great+Vibes&display=swap" rel="stylesheet">
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      color: white;
      height: 100vh;
      overflow: hidden;
    }

    .container {
      display: grid;
      grid-template-rows: auto 1fr auto;
      height: 100vh;
      padding: 20px;
    }

    header {
      text-align: center;
      padding: 10px 0;
    }

    header h1 {
      font-family: 'Great Vibes', cursive;
      font-size: 3.2rem;
      letter-spacing: 2px;
    }

    header p {
      opacity: 0.9;
      font-size: 0.95rem;
      margin-top: 5px;
    }

    .content {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 20px;
    }

    .box {
      background: rgba(255,255,255,0.18);
      border-radius: 22px;
      padding: 20px;
      backdrop-filter: blur(8px);
      box-shadow: 0 8px 25px rgba(0,0,0,0.2);
      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    .box h2 {
      font-size: 1.2rem;
      margin-bottom: 10px;
      text-align: center;
      font-weight: 600;
    }

    .story p, .letter p {
      font-size: 0.9rem;
      line-height: 1.7;
      text-align: center;
    }

    .timer {
      text-align: center;
      font-size: 1.5rem;
      font-weight: 700;
      margin-top: 10px;
    }

    .quotes {
      font-style: italic;
      text-align: center;
      font-size: 0.95rem;
      animation: fade 6s infinite;
    }

    footer {
      text-align: center;
      font-size: 0.8rem;
      opacity: 0.9;
      padding-top: 10px;
    }

    /* Hearts */
    .heart {
      position: fixed;
      width: 12px;
      height: 12px;
      background: #ff2e63;
      transform: rotate(45deg);
      animation: float 6s linear infinite;
    }
    .heart::before, .heart::after {
      content: '';
      width: 12px;
      height: 12px;
      background: #ff2e63;
      border-radius: 50%;
      position: absolute;
    }
    .heart::before { top: -6px; left: 0; }
    .heart::after { left: -6px; top: 0; }

    @keyframes float {
      0% { transform: translateY(100vh) rotate(45deg); opacity: 1; }
      100% { transform: translateY(-10vh) rotate(45deg); opacity: 0; }
    }

    @keyframes fade {
      0% {opacity: 0;}
      10% {opacity: 1;}
      90% {opacity: 1;}
      100% {opacity: 0;}
    }

    @media (max-width: 768px) {
      .content { grid-template-columns: 1fr; }
      body { overflow-y: auto; }
    }
  </style>
</head>
<body>

<div class="container">

  <header>
    <h1>Okta ❤ Eva</h1>
    <p id="typing"></p>
  </header>

  <div class="content">

    <div class="box story">
      <h2>Our Story</h2>
      <p>
        Dari semua kemungkinan di dunia ini, aku bersyukur karena semesta memilih kamu untuk hadir di hidup aku.  
        Kamu bukan sekadar seseorang, kamu adalah rumah. Tempat aku pulang, tempat aku tenang, tempat aku merasa utuh.
      </p>
    </div>

    <div class="box">
      <h2>Time With You</h2>
      <div class="timer" id="timer">Loading...</div>
    </div>

    <div class="box">
      <h2>Words From My Heart</h2>
      <div class="quotes" id="quotes">
        Aku jatuh cinta setiap hari, pada orang yang sama.
      </div>
    </div>

    <div class="box letter">
      <h2>For You, Eva 💌</h2>
      <p>
        Hai Eva…<br><br>
        Terima kasih sudah hadir, bertahan, dan memilih aku setiap hari.  
        Aku nggak minta dunia, aku cuma minta kamu.  
        <br><br>
        Aku sayang kamu. Lebih dari kemarin, kurang dari besok. ❤
      </p>
    </div>

  </div>

  <footer>
    Made with ❤ by Okta for Eva
  </footer>

</div>

<script>
  const startDate = new Date('2025-10-18T00:00:00');
  const timerEl = document.getElementById('timer');

  function updateTimer() {
    const now = new Date();
    const diff = now - startDate;

    const days = Math.floor(diff / (1000 * 60 * 60 * 24));
    const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
    const minutes = Math.floor((diff / (1000 * 60)) % 60);
    const seconds = Math.floor((diff / 1000) % 60);

    timerEl.innerHTML = `${days} hari ${hours} jam ${minutes} menit ${seconds} detik`;
  }
  setInterval(updateTimer, 1000);
  updateTimer();

  const texts = [
    "Every love story is beautiful, but ours is my favorite.",
    "Aku jatuh cinta pada senyummu, tenang pada pelukmu.",
    "Kalau disuruh pilih lagi, aku tetap pilih kamu.",
    "Kamu bukan pilihan, kamu tujuan."
  ];
  let textIndex = 0;
  const typingEl = document.getElementById('typing');

  function typeText() {
    typingEl.innerHTML = texts[textIndex];
    textIndex = (textIndex + 1) % texts.length;
  }
  setInterval(typeText, 4000);
  typeText();

  const quoteList = [
    "Aku jatuh cinta setiap hari, pada orang yang sama.",
    "Kamu adalah alasan aku percaya cinta.",
    "Bersamamu, hal sederhana jadi istimewa.",
    "Aku nggak butuh sempurna, aku butuh kamu."
  ];
  let qIndex = 0;
  const quoteEl = document.getElementById('quotes');

  setInterval(() => {
    quoteEl.innerHTML = quoteList[qIndex];
    qIndex = (qIndex + 1) % quoteList.length;
  }, 5000);

  function createHeart() {
    const heart = document.createElement('div');
    heart.classList.add('heart');
    heart.style.left = Math.random() * 100 + 'vw';
    heart.style.animationDuration = (Math.random() * 3 + 3) + 's';
    document.body.appendChild(heart);

    setTimeout(() => { heart.remove(); }, 6000);
  }
  setInterval(createHeart, 600);
</script>

</body>
</html>
