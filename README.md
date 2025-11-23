<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Mealting Maths — Fun Arithmetic (Grade 1–10)</title>

<!--
  Single-file site:
  - Animated boundary (gradient + moving dashes)
  - Left & right floating "characters" (image fallback to SVG)
  - Grade selector that teleports to sections (same page)
  - Sample quiz sections for Grade 1..10 (replace with your questions)
  - Friendly, colorful and slightly cartoon-themed style
-->

<style>
  :root{
    --bg:#f7fbff;
    --card:#ffffff;
    --accent1:#ff6f3c;
    --accent2:#00b7c2;
    --muted:#6b7280;
    --green:#23c48a;
    --shadow: 0 8px 24px rgba(15,23,42,0.08);
    --corner: 20px;
  }

  /* PAGE BOUNDARY (animated gradient + dashed border) */
  html,body{height:100%; margin:0; background:var(--bg); font-family:Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;}
  .page-frame{
    min-height:100vh;
    display:flex;
    flex-direction:column;
    align-items:center;
    padding:36px;
    box-sizing:border-box;
    position:relative;
    overflow-x:hidden;
  }

  /* animated outer ring */
  .frame-border {
    position:absolute;
    inset:8px;
    border-radius:28px;
    pointer-events:none;
    z-index:0;
    padding:6px;
    box-sizing:border-box;
    background:linear-gradient(90deg, rgba(255,111,60,0.12), rgba(0,183,194,0.08) 40%, rgba(255,207,102,0.06));
    filter:drop-shadow(0 6px 24px rgba(0,0,0,0.06));
    animation: slow-rotate 14s linear infinite;
  }
  .frame-border::after{
    content:"";
    position:absolute; inset:6px; border-radius:20px;
    border: 4px dashed rgba(0,0,0,0.06);
    mix-blend-mode: multiply;
  }
  @keyframes slow-rotate { from {transform: rotate(0);} to { transform: rotate(360deg);} }

  /* Container card */
  .site {
    width:100%;
    max-width:1100px;
    background: linear-gradient(180deg, rgba(255,255,255,0.98), rgba(255,255,255,0.96));
    border-radius:var(--corner);
    box-shadow:var(--shadow);
    z-index:1;
    overflow:hidden;
    position:relative;
  }

  /* Header */
  header {
    display:flex;
    gap:16px;
    align-items:center;
    padding:22px 28px;
    background: linear-gradient(90deg, rgba(255,111,60,0.08), rgba(0,183,194,0.06));
    border-bottom: 1px solid rgba(0,0,0,0.03);
  }
  .brand {
    display:flex; gap:12px; align-items:center;
  }
  .logo {
    width:64px; height:64px; border-radius:14px;
    background: linear-gradient(135deg,var(--accent1),var(--accent2));
    display:flex; align-items:center; justify-content:center;
    color:white; font-weight:800; font-size:22px; box-shadow: 0 6px 18px rgba(0,0,0,0.12);
  }
  .brand h1 { margin:0; font-size:20px; color:#0f1724;}
  .brand p { margin:0; color:var(--muted); font-size:13px; }

  nav { margin-left:auto; display:flex; gap:8px; align-items:center; }
  nav a { text-decoration:none; padding:8px 12px; border-radius:10px; color:#0f1724; font-weight:600; background:transparent; transition:all .2s ease; }
  nav a:hover { background: rgba(0,0,0,0.04); transform:translateY(-2px); }

  /* Header action buttons */
  .btn {
    background:var(--accent1); color:white; padding:9px 14px; border-radius:10px; text-decoration:none; font-weight:700; box-shadow: 0 6px 12px rgba(255,111,60,0.12);
  }
  .btn.secondary { background: var(--accent2); box-shadow: 0 6px 12px rgba(0,183,194,0.12); }

  /* top-floating characters (left/right) */
  .character {
    position:absolute; top:24px; width:120px; height:120px; z-index:2; pointer-events:none;
    transform-origin:center;
    animation: floaty 6s ease-in-out infinite;
  }
  .character.left { left:-10px; }
  .character.right { right:-10px; animation-delay: 1.2s; }
  @keyframes floaty { 0% { transform: translateY(0) rotate(-3deg); } 50% { transform: translateY(-14px) rotate(3deg);} 100% { transform: translateY(0) rotate(-3deg);} }

  /* Layout body */
  .content {
    padding:28px;
    display:grid;
    grid-template-columns: 1fr;
    gap:20px;
  }

  /* hero panel */
  .hero {
    display:flex;
    gap:20px;
    align-items:center;
    padding:22px;
    border-radius:14px;
    background: linear-gradient(90deg, rgba(255,239,225,0.8), rgba(227,247,255,0.8));
  }
  .hero-left { flex:1; }
  .hero-right { width:260px; display:flex; align-items:center; justify-content:center; }

  .intro { font-size:18px; color:#053047; margin:10px 0 0 0; line-height:1.5; }
  .tag { background: rgba(255,111,60,0.12); color:var(--accent1); display:inline-block; padding:6px 10px; border-radius:999px; font-weight:700; font-size:12px; }

  /* grade selector card */
  .grade-card {
    margin-top:12px;
    background: white;
    padding:12px;
    border-radius:12px;
    box-shadow: 0 6px 18px rgba(0,0,0,0.04);
    display:flex;
    gap:12px;
    align-items:center;
  }
  .grade-card select {
    padding:10px 12px; border-radius:8px; border:1px solid #e6edf2; font-size:16px;
  }
  .grade-card button { padding:10px 16px; border-radius:10px; border:none; cursor:pointer; background:var(--accent1); color:white; font-weight:700; }

  /* quizzes grid */
  .quizzes {
    display:grid;
    grid-template-columns: repeat(auto-fit,minmax(320px,1fr));
    gap:18px;
  }

  .quiz-section {
    background:var(--card);
    padding:18px;
    border-radius:14px;
    box-shadow: 0 8px 20px rgba(12,18,30,0.04);
    position:relative;
    overflow:visible;
  }

  .quiz-section h3 { margin:0 0 8px 0; color:#0f1724; }
  .quiz-box { background: linear-gradient(180deg,#fff,#fbfdff); border-radius:12px; padding:12px; border:1px solid rgba(0,0,0,0.03); }
  .question { margin:10px 0; font-weight:600; }

  /* submit/button style inside quizzes */
  .submit-btn {
    display:inline-block; margin-top:10px; padding:8px 12px; border-radius:10px; background:var(--green); color:white; font-weight:700; border:none; cursor:pointer;
  }

  /* small footer */
  footer { padding:18px; text-align:center; color:var(--muted); font-size:13px; }

  /* responsive */
  @media (max-width:720px){
    .hero { flex-direction:column; align-items:flex-start; }
    .hero-right { width:100%; }
    .character { display:none; }
  }

  /* little entrance animation for cards */
  .quiz-section { transform: translateY(8px); opacity:0; animation: cardIn .6s ease forwards; }
  .quiz-section:nth-child(1){ animation-delay: 0.05s }
  .quiz-section:nth-child(2){ animation-delay: 0.1s }
  .quiz-section:nth-child(3){ animation-delay: 0.15s }
  .quiz-section:nth-child(4){ animation-delay: 0.2s }
  @keyframes cardIn { to { transform:none; opacity:1; } }

  /* playful sparkle near logo */
  .sparkle { width:8px; height:8px; background: #fff; border-radius:50%; box-shadow: 0 0 10px rgba(255,255,255,0.9); position:relative; left:6px; top:-8px; animation: blink 2s infinite; }
  @keyframes blink { 0%,100%{ opacity:0.2 } 50%{ opacity:1 } }

  /* small style for answers */
  .options label { display:block; padding:6px 8px; border-radius:8px; margin:6px 0; background:rgba(0,0,0,0.03); cursor:pointer; }
  .options input { margin-right:8px; }

</style>
</head>
<body>

<div class="page-frame">
  <div class="frame-border"></div>

  <div class="site" role="main">

    <!-- animated characters: left & right.
         If you have real images place them in images/shinchan.png and images/doraemon.png.
         The JS will try to load those images; if not found, built-in SVG avatars appear. -->
    <div class="character left" id="char-left" aria-hidden="true"></div>
    <div class="character right" id="char-right" aria-hidden="true"></div>

    <header>
      <div class="brand">
        <div class="logo">MM</div>
        <div>
          <h1>Mealting Maths</h1>
          <p>Colourful arithmetic quizzes — Grades 1 to 10</p>
        </div>
      </div>

      <nav aria-label="Main navigation">
        <a href="#grades" onclick="document.getElementById('selector').scrollIntoView({behavior:'smooth'})">Choose Grade</a>
        <a href="#quizzes" onclick="document.getElementById('quizzes').scrollIntoView({behavior:'smooth'})">All Quizzes</a>
        <a href="#feedback" onclick="document.getElementById('feedback').scrollIntoView({behavior:'smooth'})">Feedback</a>
        <a class="btn" href="#about" onclick="document.getElementById('about').scrollIntoView({behavior:'smooth'})">About Us</a>
      </nav>
    </header>

    <div class="content">

      <!-- HERO -->
      <section class="hero" id="home" aria-labelledby="site-intro">
        <div class="hero-left">
          <span class="tag">Free • Colorful • Student-friendly</span>
          <h2 id="site-intro" style="margin:10px 0 6px 0; font-size:22px">Make arithmetic fun — one quiz at a time</h2>
          <p class="intro">Mealting Maths has short, smart quizzes for Grades 1–10. Pick your grade and jump straight to the questions — no logins, no fees.</p>

          <div class="grade-card" id="selector" style="margin-top:12px;">
            <select id="gradeSelectInline" aria-label="Select grade">
              <option value="">-- Choose Grade --</option>
              <option value="grade1">Grade 1</option>
              <option value="grade2">Grade 2</option>
              <option value="grade3">Grade 3</option>
              <option value="grade4">Grade 4</option>
              <option value="grade5">Grade 5</option>
              <option value="grade6">Grade 6</option>
              <option value="grade7">Grade 7</option>
              <option value="grade8">Grade 8</option>
              <option value="grade9">Grade 9</option>
              <option value="grade10">Grade 10</option>
            </select>
            <button id="goBtn" onclick="jumpToGrade()">Go 🚀</button>
          </div>
        </div>

        <div class="hero-right">
          <!-- decorative panel -->
          <div style="width:220px; height:160px; border-radius:12px; background:linear-gradient(180deg,#fff,#fff8f0); display:flex; align-items:center; justify-content:center; box-shadow: 0 8px 20px rgba(0,0,0,0.06);">
            <div style="text-align:center;">
              <div style="font-weight:800; font-size:28px; color:var(--accent1)">Take a Quiz</div>
              <div style="color:var(--muted); font-size:13px; margin-top:6px;">Quick, timed-free practice</div>
            </div>
          </div>
        </div>
      </section>

      <!-- QUIZZES GRID -->
      <section id="quizzes" class="quizzes" aria-label="All quizzes">

        <!-- Grade sections: each has id: grade1 ... grade10 -->
        <!-- Grade 1 -->
        <article class="quiz-section" id="grade1" tabindex="-1" aria-labelledby="g1title">
          <h3 id="g1title">Grade 1 — Mini Quiz</h3>
          <div class="quiz-box">
            <div class="question">1) 2 + 3 = ?</div>
            <div class="options">
              <label><input type="radio" name="g1q1" value="4">4</label>
              <label><input type="radio" name="g1q1" value="5">5</label>
              <label><input type="radio" name="g1q1" value="6">6</label>
            </div>

            <div class="question">2) Which number comes next: 1,2,3, _ ?</div>
            <div class="options">
              <label><input type="radio" name="g1q2" value="4">4</label>
              <label><input type="radio" name="g1q2" value="5">5</label>
              <label><input type="radio" name="g1q2" value="6">6</label>
            </div>

            <button class="submit-btn" onclick="checkScore('g1', ['g1q1','g1q2'], ['5','4'], 'g1res')">Submit</button>
            <div id="g1res" style="margin-top:8px; font-weight:700;"></div>
          </div>
        </article>

        <!-- Grade 2 -->
        <article class="quiz-section" id="grade2" tabindex="-1" aria-labelledby="g2title">
          <h3 id="g2title">Grade 2 — Mini Quiz</h3>
          <div class="quiz-box">
            <div class="question">1) 24 + 13 = ?</div>
            <div class="options">
              <label><input type="radio" name="g2q1" value="37">37</label>
              <label><input type="radio" name="g2q1" value="36">36</label>
              <label><input type="radio" name="g2q1" value="38">38</label>
            </div>

            <div class="question">2) Value of 5 in 452 is?</div>
            <div class="options">
              <label><input type="radio" name="g2q2" value="500">500</label>
              <label><input type="radio" name="g2q2" value="50">50</label>
              <label><input type="radio" name="g2q2" value="5">5</label>
            </div>

            <button class="submit-btn" onclick="checkScore('g2', ['g2q1','g2q2'], ['37','50'], 'g2res')">Submit</button>
            <div id="g2res" style="margin-top:8px; font-weight:700;"></div>
          </div>
        </article>

        <!-- Grade 3 -->
        <article class="quiz-section" id="grade3" tabindex="-1" aria-labelledby="g3title">
          <h3 id="g3title">Grade 3 — Mini Quiz</h3>
          <div class="quiz-box">
            <div class="question">1) 45 ÷ 5 = ?</div>
            <div class="options">
              <label><input type="radio" name="g3q1" value="9">9</label>
              <label><input type="radio" name="g3q1" value="8">8</label>
            </div>
            <div class="question">2) 7 × 8 = ?</div>
            <div class="options">
              <label><input type="radio" name="g3q2" value="56">56</label>
              <label><input type="radio" name="g3q2" value="54">54</label>
            </div>

            <button class="submit-btn" onclick="checkScore('g3', ['g3q1','g3q2'], ['9','56'], 'g3res')">Submit</button>
            <div id="g3res" style="margin-top:8px; font-weight:700;"></div>
          </div>
        </article>

        <!-- Grade 4 -->
        <article class="quiz-section" id="grade4" tabindex="-1" aria-labelledby="g4title">
          <h3 id="g4title">Grade 4 — Mini Quiz</h3>
          <div class="quiz-box">
            <div class="question">1) 23 × 4 = ?</div>
            <div class="options">
              <label><input type="radio" name="g4q1" value="92">92</label>
              <label><input type="radio" name="g4q1" value="82">82</label>
            </div>
            <div class="question">2) 378 + 245 = ?</div>
            <div class="options">
              <label><input type="radio" name="g4q2" value="623">623</label>
              <label><input type="radio" name="g4q2" value="613">613</label>
            </div>

            <button class="submit-btn" onclick="checkScore('g4', ['g4q1','g4q2'], ['92','623'], 'g4res')">Submit</button>
            <div id="g4res" style="margin-top:8px; font-weight:700;"></div>
          </div>
        </article>

        <!-- Grade 5 -->
        <article class="quiz-section" id="grade5" tabindex="-1" aria-labelledby="g5title">
          <h3 id="g5title">Grade 5 — Mini Quiz</h3>
          <div class="quiz-box">
            <div class="question">1) LCM of 12 and 18?</div>
            <div class="options">
              <label><input type="radio" name="g5q1" value="36">36</label>
              <label><input type="radio" name="g5q1" value="24">24</label>
            </div>
            <div class="question">2) 35% of 200 = ?</div>
            <div class="options">
              <label><input type="radio" name="g5q2" value="70">70</label>
              <label><input type="radio" name="g5q2" value="65">65</label>
            </div>

            <button class="submit-btn" onclick="checkScore('g5', ['g5q1','g5q2'], ['36','70'], 'g5res')">Submit</button>
            <div id="g5res" style="margin-top:8px; font-weight:700;"></div>
          </div>
        </article>

        <!-- Grade 6 -->
        <article class="quiz-section" id="grade6" tabindex="-1" aria-labelledby="g6title">
          <h3 id="g6title">Grade 6 — Mini Quiz</h3>
          <div class="quiz-box">
            <div class="question">1) HCF of 36 and 48?</div>
            <div class="options">
              <label><input type="radio" name="g6q1" value="12">12</label>
              <label><input type="radio" name="g6q1" value="6">6</label>
            </div>
            <div class="question">2) 5 × (2 + 3) − 4 = ?</div>
            <div class="options">
              <label><input type="radio" name="g6q2" value="21">21</label>
              <label><input type="radio" name="g6q2" value="18">18</label>
            </div>

            <button class="submit-btn" onclick="checkScore('g6', ['g6q1','g6q2'], ['12','21'], 'g6res')">Submit</button>
            <div id="g6res" style="margin-top:8px; font-weight:700;"></div>
          </div>
        </article>

        <!-- Grade 7 -->
        <article class="quiz-section" id="grade7" tabindex="-1" aria-labelledby="g7title">
          <h3 id="g7title">Grade 7 — Mini Quiz</h3>
          <div class="quiz-box">
            <div class="question">1) Simplify: (3² × 2³) ÷ 6 = ?</div>
            <div class="options">
              <label><input type="radio" name="g7q1" value="12">12</label>
              <label><input type="radio" name="g7q1" value="24">24</label>
            </div>
            <div class="question">2) Probability: 5 red, 3 blue, 2 green. P(red) = ?</div>
            <div class="options">
              <label><input type="radio" name="g7q2" value="1/2">1/2</label>
              <label><input type="radio" name="g7q2" value="5/10">5/10</label>
            </div>

            <button class="submit-btn" onclick="checkScore('g7', ['g7q1','g7q2'], ['12','1/2'], 'g7res')">Submit</button>
            <div id="g7res" style="margin-top:8px; font-weight:700;"></div>
          </div>
        </article>

        <!-- Grade 8 -->
        <article class="quiz-section" id="grade8" tabindex="-1" aria-labelledby="g8title">
          <h3 id="g8title">Grade 8 — Challenge</h3>
          <div class="quiz-box">
            <div class="question">1) Simplify: (4x - 3)² → choose correct expanded form?</div>
            <div class="options">
              <label><input type="radio" name="g8q1" value="16x² - 24x + 9">16x² - 24x + 9</label>
              <label><input type="radio" name="g8q1" value="16x² - 9">16x² - 9</label>
            </div>

            <button class="submit-btn" onclick="checkScore('g8', ['g8q1'], ['16x² - 24x + 9'], 'g8res')">Submit</button>
            <div id="g8res" style="margin-top:8px; font-weight:700;"></div>
          </div>
        </article>

        <!-- Grade 9 -->
        <article class="quiz-section" id="grade9" tabindex="-1" aria-labelledby="g9title">
          <h3 id="g9title">Grade 9 — Test Your Logic</h3>
          <div class="quiz-box">
            <div class="question">1) Solve x² + 5x + 6 = 0; roots are?</div>
            <div class="options">
              <label><input type="radio" name="g9q1" value="-2,-3">-2, -3</label>
              <label><input type="radio" name="g9q1" value="2,3">2, 3</label>
            </div>

            <button class="submit-btn" onclick="checkScore('g9', ['g9q1'], ['-2,-3'], 'g9res')">Submit</button>
            <div id="g9res" style="margin-top:8px; font-weight:700;"></div>
          </div>
        </article>

        <!-- Grade 10 -->
        <article class="quiz-section" id="grade10" tabindex="-1" aria-labelledby="g10title">
          <h3 id="g10title">Grade 10 — Final Boss</h3>
          <div class="quiz-box">
            <div class="question">1) If x² − 9x + 20 = 0, roots are?</div>
            <div class="options">
              <label><input type="radio" name="g10q1" value="4,5">4, 5</label>
              <label><input type="radio" name="g10q1" value="2,10">2, 10</label>
            </div>

            <button class="submit-btn" onclick="checkScore('g10', ['g10q1'], ['4,5'], 'g10res')">Submit</button>
            <div id="g10res" style="margin-top:8px; font-weight:700;"></div>
          </div>
        </article>

      </section>

      <!-- Feedback / About -->
      <section id="feedback" class="quiz-section" style="border-radius:14px;">
        <h3>Feedback</h3>
        <p>We use Google Forms for feedback (embedded). Put your form link into the iframe src below to enable it on your site.</p>
        <div style="border-radius:12px; overflow:hidden; border:1px solid rgba(0,0,0,0.04);">
          <iframe id="feedbackFrame" src="https://docs.google.com/forms/d/e/1FAIpQLSf8zt6PB5Fz2ZlhWNwRFdu_ED9dGMgbzNrli7twqx-nB0AlVA/viewform?embedded=true" width="100%" height="450" style="border:0;"></iframe>
        </div>
      </section>

      <section id="about" class="quiz-section" style="border-radius:14px;">
        <h3>About Mealting Maths</h3>
        <p>Mealting Maths is built by <strong>Laksh Agarwal</strong> (Grade 7). The site is free and focused on arithmetic practice for Grades 1–10. My dream is to become an entrepreneur and make learning fun for everyone!</p>
      </section>

    </div>

    <footer>
      © Mealting Maths • Free for students • Built with ❤️ by Laksh
    </footer>

  </div>
</div>

<script>
/* ---------- Character rendering:
   - Try to load images/images named shinchan.png and doraemon.png
   - If available, use them. If not, fall back to simple SVG avatars created on the fly.
*/

function createSVGAvatar(kind){
  // returns an HTML string for a simple, original, friendly avatar (not copyrighted)
  if(kind === 'shin'){
    return `
      <svg width="120" height="120" viewBox="0 0 120 120" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
        <defs><linearGradient id="g1" x1="0" x2="1"><stop offset="0" stop-color="#ffd27a"/><stop offset="1" stop-color="#ff9d6b"/></linearGradient></defs>
        <rect width="120" height="120" rx="18" fill="url(#g1)"/>
        <circle cx="60" cy="44" r="20" fill="#fff7e6" />
        <circle cx="50" cy="40" r="3" fill="#232323" /><circle cx="70" cy="40" r="3" fill="#232323" />
        <path d="M48 52 q12 12 24 0" stroke="#c14b2a" stroke-width="3" fill="none" stroke-linecap="round"/>
        <rect x="30" y="76" width="60" height="18" rx="6" fill="#fff" opacity="0.6"/>
        <text x="60" y="90" text-anchor="middle" font-weight="800" font-size="12" fill="#b94e28">Shin</text>
      </svg>`;
  } else { // dora style
    return `
      <svg width="120" height="120" viewBox="0 0 120 120" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
        <defs><linearGradient id="g2" x1="0" x2="1"><stop offset="0" stop-color="#9ee7ff"/><stop offset="1" stop-color="#67d0e6"/></linearGradient></defs>
        <rect width="120" height="120" rx="18" fill="url(#g2)"/>
        <circle cx="60" cy="46" r="26" fill="#fff"/>
        <circle cx="48" cy="42" r="3" fill="#111"/><circle cx="72" cy="42" r="3" fill="#111"/>
        <path d="M48 56 q12 12 24 0" stroke="#0b7285" stroke-width="3" fill="none" stroke-linecap="round"/>
        <rect x="30" y="76" width="60" height="18" rx="6" fill="#fff" opacity="0.6"/>
        <text x="60" y="90" text-anchor="middle" font-weight="800" font-size="12" fill="#046b79">Dora</text>
      </svg>`;
  }
}

function loadCharacterElements() {
  const left = document.getElementById('char-left');
  const right = document.getElementById('char-right');

  // Try to load external images (if you placed files at images/shinchan.png & images/doraemon.png)
  const shinImg = new Image();
  shinImg.src = 'images/shinchan.png';
  shinImg.alt = 'Shinchan';
  shinImg.onload = () => {
    shinImg.style.width='100%';
    shinImg.style.height='100%';
    shinImg.style.objectFit='contain';
    left.appendChild(shinImg);
  };
  shinImg.onerror = () => { left.innerHTML = createSVGAvatar('shin'); };

  const doraImg = new Image();
  doraImg.src = 'images/doraemon.png';
  doraImg.alt = 'Doraemon';
  doraImg.onload = () => {
    doraImg.style.width='100%';
    doraImg.style.height='100%';
    doraImg.style.objectFit='contain';
    right.appendChild(doraImg);
  };
  doraImg.onerror = () => { right.innerHTML = createSVGAvatar('dora'); };
}

/* Smooth scroll (teleport) to selected grade */
function jumpToGrade(){
  const sel = document.getElementById('gradeSelectInline');
  const val = sel.value;
  if(!val){ alert('Please choose a grade first 🙂'); return; }
  const el = document.getElementById(val);
  if(!el){ alert('That grade is not available yet.'); return; }
  el.scrollIntoView({behavior:'smooth', block:'start'});
  // set focus for keyboard users
  setTimeout(()=> el.focus({preventScroll:true}), 600);
}

/* Single generic checkScore function
   - sectionId: used for console/logging
   - questionNames: array of input name attributes (strings)
   - correctAnswers: array of strings that exactly match the chosen value(s)
   - resultId: id of element to show result text
*/
function checkScore(sectionId, questionNames, correctAnswers, resultId){
  let score = 0;
  for(let i=0;i<questionNames.length;i++){
    const name = questionNames[i];
    const sel = document.querySelector(`input[name="${name}"]:checked`);
    if(!sel) continue;
    const val = sel.value;
    if(val === correctAnswers[i]) score++;
  }
  const out = document.getElementById(resultId);
  out.textContent = `You scored ${score} out of ${questionNames.length} ✓`;
  // small celebratory animation
  out.style.color = score === questionNames.length ? 'var(--green)' : '#333';
}

/* QUICK ACCESS: allow top nav grade selector also to teleport */
document.addEventListener('DOMContentLoaded',()=>{
  loadCharacterElements();

  // enable pressing Enter on select to jump
  const sel = document.getElementById('gradeSelectInline');
  sel.addEventListener('keydown', (e)=>{ if(e.key === 'Enter'){ jumpToGrade(); } });

  // progressive reveal: set focusable for sections
  ['grade1','grade2','grade3','grade4','grade5','grade6','grade7','grade8','grade9','grade10'].forEach(id=>{
    const el = document.getElementById(id);
    if(el) el.setAttribute('tabindex','-1');
  });
});
</script>

</body>
</html>
