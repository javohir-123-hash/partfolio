<!DOCTYPE html>
<html lang="uz">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Ism Familiya — Portfolio</title>
<meta name="description" content="Ism Familiya — shaxsiy portfolio">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,500;12..96,800&family=Instrument+Sans:wght@400;500&display=swap" rel="stylesheet">
<link rel="stylesheet" href="style.css">
</head>
<body>
<style>
  :root {
  --paper: #ECEAF3;
  --ink: #1D1B3A;
  --muted: #5E5C7A;
  --cobalt: #2B4BFF;
  --mint: #CFE8DC;
  --line: #C9C6DA;
  --display: "Bricolage Grotesque", "Segoe UI", system-ui, sans-serif;
  --body: "Instrument Sans", "Segoe UI", system-ui, sans-serif;
}
* { box-sizing: border-box; margin: 0; }
html { scroll-behavior: smooth; }
body {
  background: var(--paper);
  color: var(--ink);
  font: 400 1.0625rem/1.65 var(--body);
  -webkit-font-smoothing: antialiased;
}
a { color: inherit; }
a:focus-visible, button:focus-visible { outline: 3px solid var(--cobalt); outline-offset: 3px; }
.wrap { max-width: 1080px; margin: 0 auto; padding: 0 1.5rem; }

/* Header */
header { padding: 1.5rem 0; }
header .wrap { display: flex; justify-content: space-between; align-items: center; gap: 1rem; flex-wrap: wrap; }
.logo { font: 800 1.1rem var(--display); text-decoration: none; }
nav { display: flex; gap: 1.5rem; }
nav a { text-decoration: none; color: var(--muted); font-weight: 500; }
nav a:hover { color: var(--cobalt); }

/* Hero */
.hero { padding: clamp(3rem, 9vw, 7rem) 0 clamp(3rem, 8vw, 6rem); }
.hero h1 {
  font: 800 clamp(2.8rem, 9vw, 7rem)/0.98 var(--display);
  letter-spacing: -0.03em;
  max-width: 14ch;
}
.hero p { margin-top: 1.75rem; max-width: 46ch; font-size: 1.2rem; color: var(--muted); }
.btn {
  display: inline-block; margin-top: 2rem; padding: 0.85rem 1.6rem;
  background: var(--cobalt); color: #fff; border-radius: 999px;
  text-decoration: none; font-weight: 500; transition: background .2s;
}
.btn:hover { background: var(--ink); }

/* Sections */
section { padding: clamp(2.5rem, 6vw, 4.5rem) 0; border-top: 1px solid var(--line); }
h2 { font: 800 clamp(1.8rem, 4vw, 2.6rem)/1.1 var(--display); letter-spacing: -0.02em; margin-bottom: 2rem; }

/* Projects: one interactive list */
.projects { list-style: none; padding: 0; }
.project { border-bottom: 1px solid var(--line); }
.project button {
  width: 100%; background: none; border: 0; cursor: pointer; text-align: left; color: inherit;
  display: flex; justify-content: space-between; align-items: baseline; gap: 1rem;
  padding: 1.4rem 0; font: 800 clamp(1.4rem, 3.5vw, 2.2rem) var(--display); letter-spacing: -0.02em;
}
.project button span { font: 400 0.95rem var(--body); color: var(--muted); letter-spacing: 0; white-space: nowrap; }
.project button:hover { color: var(--cobalt); }
.detail { display: none; padding: 0 0 1.6rem; max-width: 62ch; color: var(--muted); }
.detail a { color: var(--cobalt); font-weight: 500; }
.project.open .detail { display: block; }
.project.open button { color: var(--cobalt); }

/* About + skills */
.about { display: grid; gap: 2.5rem; grid-template-columns: 1fr; }
@media (min-width: 800px) { .about { grid-template-columns: 1.4fr 1fr; } }
.tags { display: flex; flex-wrap: wrap; gap: 0.6rem; list-style: none; padding: 0; }
.tags li { background: var(--mint); padding: 0.35rem 0.9rem; border-radius: 999px; font-weight: 500; font-size: 0.95rem; }

/* Contact */
.contact a.big {
  display: inline-block; font: 800 clamp(1.6rem, 5vw, 3.2rem) var(--display);
  letter-spacing: -0.02em; text-decoration-thickness: 3px; text-underline-offset: 6px;
  word-break: break-all;
}
.contact a.big:hover { color: var(--cobalt); }
.social { display: flex; gap: 1.5rem; margin-top: 1.5rem; flex-wrap: wrap; }
footer { padding: 2rem 0 3rem; color: var(--muted); font-size: 0.9rem; }

@media (prefers-reduced-motion: reduce) { html { scroll-behavior: auto; } * { transition: none !important; } }
</style>
<header>
  <div class="wrap">
    <a class="logo" href="#top">Ism Familiya</a>
    <nav aria-label="Asosiy menyu">
      <a href="#ishlar">Ishlar</a>
      <a href="#men-haqimda">Men haqimda</a>
      <a href="#aloqa">Aloqa</a>
    </nav>
  </div>
</header>

<main id="top">
  <div class="wrap">

    <!-- 1. HERO: ismingiz va kasbingizni o'zgartiring -->
    <div class="hero">
      <h1>Men veb-saytlar va ilovalar yarataman.</h1>
      <p>Toshkentdan turib, kichik bizneslar uchun tushunarli va tez ishlaydigan raqamli mahsulotlar qilaman.</p>
      <a class="btn" href="#ishlar">Ishlarimni ko'rish</a>
    </div>

    <!-- 2. ISHLAR: har bir loyihani o'zingiznikiga almashtiring -->
    <section id="ishlar">
      <h2>Tanlangan ishlar</h2>
      <ul class="projects" id="projects">
        <li class="project">
          <button aria-expanded="false">Kofexona buyurtma ilovasi <span>2026</span></button>
          <div class="detail">
            Mijozlar telefondan buyurtma berib, navbatsiz olib ketadigan mobil veb-ilova. Buyurtmalar 40% tezroq berila boshladi.
            <br><a href="#" target="_blank" rel="noopener">Loyihani ochish</a>
          </div>
        </li>
        <li class="project">
          <button aria-expanded="false">Moliyaviy hisob paneli <span>2025</span></button>
          <div class="detail">
            Kunlik tushum va xarajatlarni grafikda ko'rsatadigan panel. JavaScript va Chart.js asosida qurilgan.
            <br><a href="#" target="_blank" rel="noopener">Loyihani ochish</a>
          </div>
        </li>
        <li class="project">
          <button aria-expanded="false">Fotograf uchun portfolio sayti <span>2025</span></button>
          <div class="detail">
            Katta suratlar va tez yuklanish uchun optimallashtirilgan galereya sayti.
            <br><a href="#" target="_blank" rel="noopener">Loyihani ochish</a>
          </div>
        </li>
      </ul>
    </section>

    <!-- 3. MEN HAQIMDA -->
    <section id="men-haqimda">
      <div class="about">
        <div>
          <h2>Men haqimda</h2>
          <p>Men 3 yildan beri frilanser sifatida ishlayman. Mijozning maqsadini tushunib, keraksiz narsalarsiz oddiy va ishonchli yechim qilishni yoqtiraman.</p>
          <p style="margin-top:1rem">Bo'sh vaqtimda moliya va investitsiya haqida o'qiyman.</p>
        </div>
        <div>
          <h2>Ko'nikmalar</h2>
          <ul class="tags">
            <li>HTML</li><li>CSS</li><li>JavaScript</li>
            <li>React</li><li>Python</li><li>Figma</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- 4. ALOQA -->
    <section id="aloqa" class="contact">
      <h2>Birga ishlaymizmi?</h2>
      <a class="big" href="mailto:ism@example.com">ism@example.com</a>
      <div class="social">
        <a href="https://t.me/username" target="_blank" rel="noopener">Telegram</a>
        <a href="https://github.com/username" target="_blank" rel="noopener">GitHub</a>
        <a href="https://linkedin.com/in/username" target="_blank" rel="noopener">LinkedIn</a>
      </div>
    </section>

  </div>
</main>

<footer>
  <div class="wrap">© <span id="year"></span> Ism Familiya</div>
</footer>

<script>
  // Loyihalarni ochish/yopish
  document.querySelectorAll('.project button').forEach(function (btn) {
    btn.addEventListener('click', function () {
      var item = btn.parentElement;
      var open = item.classList.toggle('open');
      btn.setAttribute('aria-expanded', open);
    });
  });
  document.getElementById('year').textContent = new Date().getFullYear();
</script>
</body>
</html>
