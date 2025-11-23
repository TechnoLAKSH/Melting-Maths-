<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Mealting Maths — Grades 1–10</title>
<style>
  :root{
    --bg:#f6fbff; --card:#ffffff; --accent1:#ff6f3c; --accent2:#00b7c2;
    --muted:#6b7280; --green:#23c48a; --corner:16px; --shadow: 0 8px 24px rgba(15,23,42,0.08);
  }
  html,body{height:100%;margin:0;font-family:Inter,system-ui,Segoe UI,Roboto,Arial;background:var(--bg);color:#0f1724}
  .page {
    max-width:1150px;margin:28px auto;padding:22px;position:relative;
    border-radius:20px;background:linear-gradient(180deg,rgba(255,255,255,0.98),rgba(255,255,255,0.96));
    box-shadow:var(--shadow); overflow:hidden;
  }

  /* animated border */
  .page:before{
    content:"";position:absolute;inset:6px;border-radius:22px;
    background:linear-gradient(90deg, rgba(255,111,60,0.08), rgba(0,183,194,0.06));
    z-index:0; filter: blur(8px);
  }
  .page:after{
    content:""; position:absolute; inset:2px; border-radius:18px; pointer-events:none;
    border:4px dashed rgba(0,0,0,0.06); mix-blend-mode:multiply;
  }

  header{display:flex;align-items:center;gap:16px;padding:18px 22px;position:relative;z-index:2}
  .logo{width:72px;height:72px;border-radius:14px;background:linear-gradient(135deg,var(--accent1),var(--accent2));display:flex;align-items:center;justify-content:center;color:white;font-weight:900;font-size:22px;box-shadow:0 8px 16px rgba(0,0,0,0.08)}
  .title h1{margin:0;font-size:22px}
  .title p{margin:2px 0 0 0;color:var(--muted);font-size:13px}

  nav{margin-left:auto;display:flex;gap:10px;align-items:center}
  nav a{padding:8px 12px;border-radius:10px;text-decoration:none;color:#0f1724;font-weight:700;background:transparent}
  nav a.btn{background:var(--accent1);color:white;box-shadow:0 8px 18px rgba(255,111,60,0.12)}
  nav a.btn.secondary{background:var(--accent2);box-shadow:0 8px 18px rgba(0,183,194,0.12)}

  /* floating characters */
  .float-left,.float-right{position:absolute;top:18px;width:120px;height:120px;z-index:1;pointer-events:none;animation:floaty 6s ease-in-out infinite}
  .float-left{left:-14px;transform-origin:center}
  .float-right{right:-14px;transform-origin:center;animation-delay:1.2s}
  @keyframes floaty{0%{transform:translateY(0) rotate(-3deg)}50%{transform:translateY(-12px) rotate(3deg)}100%{transform:translateY(0) rotate(-3deg)}}

  .content{padding:18px 22px;position:relative;z-index:2}
  .hero{display:flex;gap:18px;align-items:center;background:linear-gradient(90deg,rgba(255,239,225,0.8),rgba(227,247,255,0.8));padding:18px;border-radius:12px}
  .hero-left{flex:1}
  .tag{display:inline-block;padding:6px 10px;border-radius:999px;font-weight:800;font-size:12px;background:rgba(255,111,60,0.12);color:var(--accent1)}
  .hero-left h2{margin:10px 0 6px 0}
  .hero p{margin:0;color:var(--muted)}
  .hero-right{width:220px;text-align:center}

  /* selector */
  .selector{display:flex;gap:10px;align-items:center;margin-top:12px}
  select{padding:10px;border-radius:10px;border:1px solid #e6eef2;font-size:16px}
  .go-btn{padding:10px 14px;border-radius:10px;border:none;background:var(--accent1);color:white;font-weight:800;cursor:pointer}

  /* quizzes */
  .quizzes{margin-top:20px;display:grid;grid-template-columns:repeat(auto-fit,minmax(320px,1fr));gap:18px}
  .quiz{background:var(--card);padding:14px;border-radius:12px;box-shadow:0 8px 20px rgba(12,18,30,0.04);transition:transform .12s ease}
  .quiz:hover{transform:translateY(-6px)}
  .quiz h3{margin:0 0 8px 0}
  .question{font-weight:700;margin-top:8px}
  .options label{display:block;padding:8px;border-radius:8px;margin:6px 0;background:rgba(0,0,0,0.03);cursor:pointer}
  .submit{margin-top:10px;padding:8px 12px;border-radius:10px;border:none;background:var(--accent2);color:white;font-weight:800;cursor:pointer}

  .result{margin-top:8px;font-weight:800;color:var(--green)}

  footer{margin-top:18px;padding:12px;text-align:center;color:var(--muted);font-size:13px}

  @media(max-width:760px){
    header{flex-wrap:wrap}
    .hero{flex-direction:column;align-items:flex-start}
    .float-left,.float-right{display:none}
  }
</style>
</head>
<body>

<div class="page" role="main">

  <!-- floating characters -->
  <div class="float-left" id="float-left">
    <!-- top-left Shinchan (uses your uploaded image path) -->
    <img src="/mnt/data/LAKSH .jpg" alt="Shinchan" style="width:100%;height:100%;object-fit:cover;border-radius:12px;box-shadow:0 10px 24px rgba(0,0,0,0.12)" />
  </div>

  <div class="float-right" id="float-right" aria-hidden="true">
    <!-- Doraemon-style SVG (safe avatar) -->
    <svg width="100%" height="100%" viewBox="0 0 120 120" xmlns="http://www.w3.org/2000/svg" style="border-radius:12px;box-shadow:0 10px 24px rgba(0,0,0,0.12)">
      <defs><linearGradient id="g2" x1="0" x2="1"><stop offset="0" stop-color="#9ee7ff"/><stop offset="1" stop-color="#67d0e6"/></linearGradient></defs>
      <rect width="120" height="120" rx="12" fill="url(#g2)"/>
      <circle cx="60" cy="46" r="26" fill="#fff"/>
      <circle cx="48" cy="42" r="3" fill="#111"/><circle cx="72" cy="42" r="3" fill="#111"/>
      <path d="M48 56 q12 12 24 0" stroke="#046b79" stroke-width="3" fill="none" stroke-linecap="round"/>
      <rect x="30" y="76" width="60" height="18" rx="6" fill="#fff" opacity="0.6"/>
      <text x="60" y="90" text-anchor="middle" font-weight="800" font-size="12" fill="#046b79">Dora</text>
    </svg>
  </div>

  <header>
    <div class="logo">MM</div>
    <div class="title">
      <h1>Mealting Maths</h1>
      <p>Colourful arithmetic quizzes for Grades 1–10 — free & friendly</p>
    </div>

    <nav aria-label="Main">
      <a href="#quizzes" onclick="document.getElementById('quizzes').scrollIntoView({behavior:'smooth'})">All Quizzes</a>
      <a class="btn" href="#about" onclick="document.getElementById('about').scrollIntoView({behavior:'smooth'})">About</a>
      <a class="btn secondary" href="#feedback" onclick="document.getElementById('feedback').scrollIntoView({behavior:'smooth'})">Feedback</a>
    </nav>
  </header>

  <div class="content">

    <section class="hero" aria-labelledby="intro">
      <div class="hero-left">
        <div class="tag">Free • Fun • No login</div>
        <h2 id="intro">Make arithmetic fun — one quiz at a time</h2>
        <p>Choose your grade below and teleport right to your quiz. Each grade has seven quick MCQs — try them and check your score instantly.</p>

        <div class="selector" id="selector">
          <select id="gradeSelect" aria-label="Choose Grade">
            <option value="">-- Choose Grade --</option>
            <option value="grade1">Grade 1</option><option value="grade2">Grade 2</option>
            <option value="grade3">Grade 3</option><option value="grade4">Grade 4</option>
            <option value="grade5">Grade 5</option><option value="grade6">Grade 6</option>
            <option value="grade7">Grade 7</option><option value="grade8">Grade 8</option>
            <option value="grade9">Grade 9</option><option value="grade10">Grade 10</option>
          </select>
          <button class="go-btn" onclick="goToGrade()">Go 🚀</button>
        </div>
      </div>

      <div class="hero-right">
        <!-- top Shinchan (same image) -->
        <img src="/mnt/data/LAKSH .jpg" alt="Shinchan" style="width:120px;height:120px;border-radius:10px;object-fit:cover;box-shadow:0 8px 20px rgba(0,0,0,0.08)">
      </div>
    </section>

    <section id="quizzes" class="quizzes" aria-label="Quizzes">

      <!-- GRADE 1 -->
      <article class="quiz" id="grade1" tabindex="-1" aria-labelledby="g1">
        <h3 id="g1">Grade 1 — 7 Questions</h3>
        <div class="quiz-inner">
          <!-- 7 MCQs -->
          <div class="question">1) 2 + 3 = ?</div>
          <div class="options"><label><input type="radio" name="g1q1" value="4">4</label><label><input type="radio" name="g1q1" value="5">5</label><label><input type="radio" name="g1q1" value="6">6</label></div>

          <div class="question">2) 4 + 4 = ?</div>
          <div class="options"><label><input type="radio" name="g1q2" value="8">8</label><label><input type="radio" name="g1q2" value="9">9</label><label><input type="radio" name="g1q2" value="7">7</label></div>

          <div class="question">3) 7 − 2 = ?</div>
          <div class="options"><label><input type="radio" name="g1q3" value="6">6</label><label><input type="radio" name="g1q3" value="5">5</label><label><input type="radio" name="g1q3" value="4">4</label></div>

          <div class="question">4) 3 + 6 = ?</div>
          <div class="options"><label><input type="radio" name="g1q4" value="8">8</label><label><input type="radio" name="g1q4" value="9">9</label><label><input type="radio" name="g1q4" value="7">7</label></div>

          <div class="question">5) 5 − 1 = ?</div>
          <div class="options"><label><input type="radio" name="g1q5" value="3">3</label><label><input type="radio" name="g1q5" value="4">4</label><label><input type="radio" name="g1q5" value="5">5</label></div>

          <div class="question">6) 1 + 8 = ?</div>
          <div class="options"><label><input type="radio" name="g1q6" value="9">9</label><label><input type="radio" name="g1q6" value="8">8</label><label><input type="radio" name="g1q6" value="10">10</label></div>

          <div class="question">7) 2 + 6 = ?</div>
          <div class="options"><label><input type="radio" name="g1q7" value="7">7</label><label><input type="radio" name="g1q7" value="8">8</label><label><input type="radio" name="g1q7" value="9">9</label></div>

          <button class="submit" onclick="gradeSubmit('g1', ['g1q1','g1q2','g1q3','g1q4','g1q5','g1q6','g1q7'], ['5','8','5','9','4','9','8'], 'res1')">Submit</button>
          <div id="res1" class="result" role="status"></div>
        </div>
      </article>

      <!-- GRADE 2 -->
      <article class="quiz" id="grade2" tabindex="-1" aria-labelledby="g2">
        <h3 id="g2">Grade 2 — 7 Questions</h3>
        <div class="quiz-inner">
          <div class="question">1) 15 + 7 = ?</div>
          <div class="options"><label><input type="radio" name="g2q1" value="21">21</label><label><input type="radio" name="g2q1" value="22">22</label><label><input type="radio" name="g2q1" value="23">23</label></div>

          <div class="question">2) 20 − 9 = ?</div>
          <div class="options"><label><input type="radio" name="g2q2" value="11">11</label><label><input type="radio" name="g2q2" value="10">10</label><label><input type="radio" name="g2q2" value="12">12</label></div>

          <div class="question">3) 6 × 3 = ?</div>
          <div class="options"><label><input type="radio" name="g2q3" value="18">18</label><label><input type="radio" name="g2q3" value="16">16</label><label><input type="radio" name="g2q3" value="20">20</label></div>

          <div class="question">4) 24 ÷ 6 = ?</div>
          <div class="options"><label><input type="radio" name="g2q4" value="3">3</label><label><input type="radio" name="g2q4" value="4">4</label><label><input type="radio" name="g2q4" value="6">6</label></div>

          <div class="question">5) 45 + 5 = ?</div>
          <div class="options"><label><input type="radio" name="g2q5" value="50">50</label><label><input type="radio" name="g2q5" value="49">49</label><label><input type="radio" name="g2q5" value="55">55</label></div>

          <div class="question">6) 7 × 5 = ?</div>
          <div class="options"><label><input type="radio" name="g2q6" value="30">30</label><label><input type="radio" name="g2q6" value="35">35</label><label><input type="radio" name="g2q6" value="25">25</label></div>

          <div class="question">7) 30 − 12 = ?</div>
          <div class="options"><label><input type="radio" name="g2q7" value="18">18</label><label><input type="radio" name="g2q7" value="20">20</label><label><input type="radio" name="g2q7" value="16">16</label></div>

          <button class="submit" onclick="gradeSubmit('g2', ['g2q1','g2q2','g2q3','g2q4','g2q5','g2q6','g2q7'], ['22','11','18','4','50','35','18'], 'res2')">Submit</button>
          <div id="res2" class="result"></div>
        </div>
      </article>

      <!-- GRADE 3 -->
      <article class="quiz" id="grade3" tabindex="-1" aria-labelledby="g3">
        <h3 id="g3">Grade 3 — 7 Questions</h3>
        <div class="quiz-inner">
          <div class="question">1) 12 × 3 = ?</div>
          <div class="options"><label><input type="radio" name="g3q1" value="36">36</label><label><input type="radio" name="g3q1" value="32">32</label></div>

          <div class="question">2) 81 ÷ 9 = ?</div>
          <div class="options"><label><input type="radio" name="g3q2" value="9">9</label><label><input type="radio" name="g3q2" value="8">8</label></div>

          <div class="question">3) 15 + 27 = ?</div>
          <div class="options"><label><input type="radio" name="g3q3" value="42">42</label><label><input type="radio" name="g3q3" value="43">43</label></div>

          <div class="question">4) 100 − 37 = ?</div>
          <div class="options"><label><input type="radio" name="g3q4" value="63">63</label><label><input type="radio" name="g3q4" value="53">53</label></div>

          <div class="question">5) 4 × 8 = ?</div>
          <div class="options"><label><input type="radio" name="g3q5" value="32">32</label><label><input type="radio" name="g3q5" value="30">30</label></div>

          <div class="question">6) 48 ÷ 6 = ?</div>
          <div class="options"><label><input type="radio" name="g3q6" value="8">8</label><label><input type="radio" name="g3q6" value="6">6</label></div>

          <div class="question">7) 7 × 7 = ?</div>
          <div class="options"><label><input type="radio" name="g3q7" value="49">49</label><label><input type="radio" name="g3q7" value="47">47</label></div>

          <button class="submit" onclick="gradeSubmit('g3', ['g3q1','g3q2','g3q3','g3q4','g3q5','g3q6','g3q7'], ['36','9','42','63','32','8','49'], 'res3')">Submit</button>
          <div id="res3" class="result"></div>
        </div>
      </article>

      <!-- GRADE 4 -->
      <article class="quiz" id="grade4" tabindex="-1" aria-labelledby="g4">
        <h3 id="g4">Grade 4 — 7 Questions</h3>
        <div class="quiz-inner">
          <div class="question">1) 23 × 4 = ?</div>
          <div class="options"><label><input type="radio" name="g4q1" value="92">92</label><label><input type="radio" name="g4q1" value="82">82</label></div>

          <div class="question">2) 144 ÷ 12 = ?</div>
          <div class="options"><label><input type="radio" name="g4q2" value="12">12</label><label><input type="radio" name="g4q2" value="14">14</label></div>

          <div class="question">3) 56 + 38 = ?</div>
          <div class="options"><label><input type="radio" name="g4q3" value="94">94</label><label><input type="radio" name="g4q3" value="84">84</label></div>

          <div class="question">4) 1000 − 457 = ?</div>
          <div class="options"><label><input type="radio" name="g4q4" value="543">543</label><label><input type="radio" name="g4q4" value="553">553</label></div>

          <div class="question">5) 9 × 9 = ?</div>
          <div class="options"><label><input type="radio" name="g4q5" value="81">81</label><label><input type="radio" name="g4q5" value="72">72</label></div>

          <div class="question">6) 63 ÷ 7 = ?</div>
          <div class="options"><label><input type="radio" name="g4q6" value="9">9</label><label><input type="radio" name="g4q6" value="8">8</label></div>

          <div class="question">7) 125 + 375 = ?</div>
          <div class="options"><label><input type="radio" name="g4q7" value="500">500</label><label><input type="radio" name="g4q7" value="450">450</label></div>

          <button class="submit" onclick="gradeSubmit('g4', ['g4q1','g4q2','g4q3','g4q4','g4q5','g4q6','g4q7'], ['92','12','94','543','81','9','500'], 'res4')">Submit</button>
          <div id="res4" class="result"></div>
        </div>
      </article>

      <!-- GRADE 5 -->
      <article class="quiz" id="grade5" tabindex="-1" aria-labelledby="g5">
        <h3 id="g5">Grade 5 — 7 Questions</h3>
        <div class="quiz-inner">
          <div class="question">1) LCM of 12 and 18 = ?</div>
          <div class="options"><label><input type="radio" name="g5q1" value="36">36</label><label><input type="radio" name="g5q1" value="24">24</label></div>

          <div class="question">2) 35% of 200 = ?</div>
          <div class="options"><label><input type="radio" name="g5q2" value="70">70</label><label><input type="radio" name="g5q2" value="75">75</label></div>

          <div class="question">3) 3/4 of 80 = ?</div>
          <div class="options"><label><input type="radio" name="g5q3" value="60">60</label><label><input type="radio" name="g5q3" value="50">50</label></div>

          <div class="question">4) 7 × 14 = ?</div>
          <div class="options"><label><input type="radio" name="g5q4" value="98">98</label><label><input type="radio" name="g5q4" value="84">84</label></div>

          <div class="question">5) 625 ÷ 25 = ?</div>
          <div class="options"><label><input type="radio" name="g5q5" value="25">25</label><label><input type="radio" name="g5q5" value="15">15</label></div>

          <div class="question">6) 11 × 11 = ?</div>
          <div class="options"><label><input type="radio" name="g5q6" value="121">121</label><label><input type="radio" name="g5q6" value="111">111</label></div>

          <div class="question">7) 1000 ÷ 8 = ?</div>
          <div class="options"><label><input type="radio" name="g5q7" value="125">125</label><label><input type="radio" name="g5q7" value="120">120</label></div>

          <button class="submit" onclick="gradeSubmit('g5', ['g5q1','g5q2','g5q3','g5q4','g5q5','g5q6','g5q7'], ['36','70','60','98','25','121','125'], 'res5')">Submit</button>
          <div id="res5" class="result"></div>
        </div>
      </article>

      <!-- GRADE 6 -->
      <article class="quiz" id="grade6" tabindex="-1" aria-labelledby="g6">
        <h3 id="g6">Grade 6 — 7 Questions</h3>
        <div class="quiz-inner">
          <div class="question">1) HCF of 36 and 48 = ?</div>
          <div class="options"><label><input type="radio" name="g6q1" value="6">6</label><label><input type="radio" name="g6q1" value="12">12</label></div>

          <div class="question">2) 5 × (2 + 3) − 4 = ?</div>
          <div class="options"><label><input type="radio" name="g6q2" value="21">21</label><label><input type="radio" name="g6q2" value="18">18</label></div>

          <div class="question">3) 25 × 4 + 100 ÷ 2 = ?</div>
          <div class="options"><label><input type="radio" name="g6q3" value="150">150</label><label><input type="radio" name="g6q3" value="100">100</label></div>

          <div class="question">4) 15² − 5² = ?</div>
          <div class="options"><label><input type="radio" name="g6q4" value="200">200</label><label><input type="radio" name="g6q4" value="100">100</label></div>

          <div class="question">5) (3/4 + 1/2) − 1/8 = ? (as fraction)</div>
          <div class="options"><label><input type="radio" name="g6q5" value="9/8">9/8</label><label><input type="radio" name="g6q5" value="1.125">1.125</label></div>

          <div class="question">6) LCM of 6 and 8 = ?</div>
          <div class="options"><label><input type="radio" name="g6q6" value="24">24</label><label><input type="radio" name="g6q6" value="48">48</label></div>

          <div class="question">7) 18 ÷ 3 + 4 = ?</div>
          <div class="options"><label><input type="radio" name="g6q7" value="10">10</label><label><input type="radio" name="g6q7" value="8">8</label></div>

          <button class="submit" onclick="gradeSubmit('g6', ['g6q1','g6q2','g6q3','g6q4','g6q5','g6q6','g6q7'], ['12','21','150','200','9/8','24','10'], 'res6')">Submit</button>
          <div id="res6" class="result"></div>
        </div>
      </article>

      <!-- GRADE 7 -->
      <article class="quiz" id="grade7" tabindex="-1" aria-labelledby="g7">
        <h3 id="g7">Grade 7 — 7 Questions</h3>
        <div class="quiz-inner">
          <div class="question">1) (3² × 2³) ÷ 6 = ?</div>
          <div class="options"><label><input type="radio" name="g7q1" value="12">12</label><label><input type="radio" name="g7q1" value="24">24</label></div>

          <div class="question">2) Solve: 2x + 3 = 15 → x = ?</div>
          <div class="options"><label><input type="radio" name="g7q2" value="6">6</label><label><input type="radio" name="g7q2" value="7">7</label></div>

          <div class="question">3) Probability: 5 red, 3 blue, 2 green. P(red) = ?</div>
          <div class="options"><label><input type="radio" name="g7q3" value="1/2">1/2</label><label><input type="radio" name="g7q3" value="5/10">5/10</label></div>

          <div class="question">4) √196 = ?</div>
          <div class="options"><label><input type="radio" name="g7q4" value="14">14</label><label><input type="radio" name="g7q4" value="13">13</label></div>

          <div class="question">5) If 2/5 of a number = 14, number = ?</div>
          <div class="options"><label><input type="radio" name="g7q5" value="35">35</label><label><input type="radio" name="g7q5" value="28">28</label></div>

          <div class="question">6) 4×3 + 5² = ?</div>
          <div class="options"><label><input type="radio" name="g7q6" value="37">37</label><label><input type="radio" name="g7q6" value="45">45</label></div>

          <div class="question">7) HCF of 48 and 64 = ?</div>
          <div class="options"><label><input type="radio" name="g7q7" value="16">16</label><label><input type="radio" name="g7q7" value="8">8</label></div>

          <button class="submit" onclick="gradeSubmit('g7', ['g7q1','g7q2','g7q3','g7q4','g7q5','g7q6','g7q7'], ['12','6','1/2','14','35','37','16'], 'res7')">Submit</button>
          <div id="res7" class="result"></div>
        </div>
      </article>

      <!-- GRADE 8 -->
      <article class="quiz" id="grade8" tabindex="-1" aria-labelledby="g8">
        <h3 id="g8">Grade 8 — 7 Questions (Challenging)</h3>
        <div class="quiz-inner">
          <div class="question">1) Expand: (4x − 3)² = ?</div>
          <div class="options"><label><input type="radio" name="g8q1" value="16x² - 24x + 9">16x² - 24x + 9</label><label><input type="radio" name="g8q1" value="16x² - 9">16x² - 9</label></div>

          <div class="question">2) If boys:girls = 3:5, girls % = ?</div>
          <div class="options"><label><input type="radio" name="g8q2" value="62.5%">62.5%</label><label><input type="radio" name="g8q2" value="60%">60%</label></div>

          <div class="question">3) 3/4 + 2/3 = ?</div>
          <div class="options"><label><input type="radio" name="g8q3" value="17/12">17/12</label><label><input type="radio" name="g8q3" value="11/12">11/12</label></div>

          <div class="question">4) Increase 20% then decrease 20% → net change?</div>
          <div class="options"><label><input type="radio" name="g8q4" value="Decrease 4%">Decrease 4%</label><label><input type="radio" name="g8q4" value="No change">No change</label></div>

          <div class="question">5) √324 = ?</div>
          <div class="options"><label><input type="radio" name="g8q5" value="18">18</label><label><input type="radio" name="g8q5" value="17">17</label></div>

          <div class="question">6) 5(2x − 3) + 4(3x + 2) = ?</div>
          <div class="options"><label><input type="radio" name="g8q6" value="22x - 7">22x - 7</label><label><input type="radio" name="g8q6" value="10x - 7">10x - 7</label></div>

          <div class="question">7) Cube of 7 = ?</div>
          <div class="options"><label><input type="radio" name="g8q7" value="343">343</label><label><input type="radio" name="g8q7" value="147">147</label></div>

          <button class="submit" onclick="gradeSubmit('g8', ['g8q1','g8q2','g8q3','g8q4','g8q5','g8q6','g8q7'], ['16x² - 24x + 9','62.5%','17/12','Decrease 4%','18','22x - 7','343'], 'res8')">Submit</button>
          <div id="res8" class="result"></div>
        </div>
      </article>

      <!-- GRADE 9 -->
      <article class="quiz" id="grade9" tabindex="-1" aria-labelledby="g9">
        <h3 id="g9">Grade 9 — 7 Questions</h3>
        <div class="quiz-inner">
          <div class="question">1) Roots of x² + 5x + 6 = 0?</div>
          <div class="options"><label><input type="radio" name="g9q1" value="-2,-3">-2, -3</label><label><input type="radio" name="g9q1" value="2,3">2, 3</label></div>

          <div class="question">2) (3² × 2³) ÷ 6 = ?</div>
          <div class="options"><label><input type="radio" name="g9q2" value="12">12</label><label><input type="radio" name="g9q2" value="8">8</label></div>

          <div class="question">3) Salary +10% then −10% → net change?</div>
          <div class="options"><label><input type="radio" name="g9q3" value="Decrease 1%">Decrease 1%</label><label><input type="radio" name="g9q3" value="No change">No change</label></div>

          <div class="question">4) If √x = 7, x + √x = ?</div>
          <div class="options"><label><input type="radio" name="g9q4" value="56">56</label><label><input type="radio" name="g9q4" value="49">49</label></div>

          <div class="question">5) (2x + 3)(2x − 3) = ?</div>
          <div class="options"><label><input type="radio" name="g9q5" value="4x² - 9">4x² - 9</label><label><input type="radio" name="g9q5" value="4x² + 9">4x² + 9</label></div>

          <div class="question">6) 0.2 as fraction = ?</div>
          <div class="options"><label><input type="radio" name="g9q6" value="1/5">1/5</label><label><input type="radio" name="g9q6" value="2/10">2/10</label></div>

          <div class="question">7) 15% of 240 = ?</div>
          <div class="options"><label><input type="radio" name="g9q7" value="36">36</label><label><input type="radio" name="g9q7" value="30">30</label></div>

          <button class="submit" onclick="gradeSubmit('g9', ['g9q1','g9q2','g9q3','g9q4','g9q5','g9q6','g9q7'], ['-2,-3','12','Decrease 1%','56','4x² - 9','1/5','36'], 'res9')">Submit</button>
          <div id="res9" class="result"></div>
        </div>
      </article>

      <!-- GRADE 10 -->
      <article class="quiz" id="grade10" tabindex="-1" aria-labelledby="g10">
        <h3 id="g10">Grade 10 — 7 Questions (Final)</h3>
        <div class="quiz-inner">
          <div class="question">1) Roots of x² − 9x + 20 = 0?</div>
          <div class="options"><label><input type="radio" name="g10q1" value="4,5">4, 5</label><label><input type="radio" name="g10q1" value="2,10">2, 10</label></div>

          <div class="question">2) (2/3) ÷ (4/9) = ?</div>
          <div class="options"><label><input type="radio" name="g10q2" value="3/2">3/2</label><label><input type="radio" name="g10q2" value="2/3">2/3</label></div>

          <div class="question">3) (x − 2)(x + 2) = ?</div>
          <div class="options"><label><input type="radio" name="g10q3" value="x² - 4">x² - 4</label><label><input type="radio" name="g10q3" value="x² + 4">x² + 4</label></div>

          <div class="question">4) Train 120 km in 2 hours. Speed in m/s = ?</div>
          <div class="options"><label><input type="radio" name="g10q4" value="16.67">16.67</label><label><input type="radio" name="g10q4" value="30">30</label></div>

          <div class="question">5) Sum of interior angles of a hexagon = ?</div>
          <div class="options"><label><input type="radio" name="g10q5" value="720°">720°</label><label><input type="radio" name="g10q5" value="540°">540°</label></div>

          <div class="question">6) Solve x/5 = 7 → x = ?</div>
          <div class="options"><label><input type="radio" name="g10q6" value="35">35</label><label><input type="radio" name="g10q6" value="12">12</label></div>

          <div class="question">7) 3x^2 − 2x when x = 2 → ?</div>
          <div class="options"><label><input type="radio" name="g10q7" value="8">8</label><label><input type="radio" name="g10q7" value="10">10</label></div>

          <button class="submit" onclick="gradeSubmit('g10', ['g10q1','g10q2','g10q3','g10q4','g10q5','g10q6','g10q7'], ['4,5','3/2','x² - 4','16.67','720°','35','8'], 'res10')">Submit</button>
          <div id="res10" class="result"></div>
        </div>
      </article>

    </section>

    <!-- feedback / about -->
    <section id="feedback" style="margin-top:18px;background:var(--card);padding:14px;border-radius:12px">
      <h3>Feedback</h3>
      <p>Embed your Google Form (or use the one you created). It will appear here when you paste the form embed link.</p>
      <div style="border-radius:10px;overflow:hidden;border:1px solid rgba(0,0,0,0.04)">
        <iframe src="https://docs.google.com/forms/d/e/1FAIpQLSf8zt6PB5Fz2ZlhWNwRFdu_ED9dGMgbzNrli7twqx-nB0AlVA/viewform?embedded=true" width="100%" height="420" style="border:0"></iframe>
      </div>
    </section>

    <section id="about" style="margin-top:18px;background:var(--card);padding:14px;border-radius:12px">
      <h3>About Mealting Maths</h3>
      <p> Hi! I'm <span class="highlight">Laksh Agarwal</span>, a Grade 7 student from <span class="highlight">India</span>. I’m the founder of <strong>Mealting Maths</strong> — a free educational website built especially for students from <strong>Grade 1 to 10</strong>. I created this platform because I truly believe that maths doesn’t have to be scary or boring. With colorful quizzes and simple design, learning numbers can actually be fun!
        </p>
        <p>
            I started <strong>Mealting Maths</strong> to give students across India and beyond a place to practice arithmetic in a joyful, stress-free way — and totally free of cost. I enjoy coding, creating websites, and helping friends understand difficult topics.
        </p>
        <p>
            My dream is to become a successful <span class="highlight">entrepreneur</span> one day — someone who builds things that make learning and life easier for everyone. <em>Mealting Maths</em> is my first step toward that dream.
        </p>
        <p><strong>Let’s melt the fear of maths — together!</strong></p>
    </div>
</body>
</html>

  </div>

  <footer>© Mealting Maths — Made with ❤️ by Laksh</footer>
</div>

<script>
  function goToGrade(){
    const sel = document.getElementById('gradeSelect');
    const id = sel.value;
    if(!id){ alert('Please choose a grade first 🙂'); return; }
    const el = document.getElementById(id);
    if(!el){ alert('That grade is not ready yet.'); return; }
    el.scrollIntoView({behavior:'smooth', block:'start'});
    setTimeout(()=> el.focus({preventScroll:true}), 500);
  }

  // generic grader: names: array of input names, answers: array of correct values, resultId: id to show result
  function gradeSubmit(section, names, answers, resultId){
    let score = 0;
    for(let i=0;i<names.length;i++){
      const name = names[i];
      const selected = document.querySelector('input[name="'+name+'"]:checked');
      if(!selected) continue;
      const val = selected.value;
      if(val === answers[i]) score++;
    }
    const out = document.getElementById(resultId);
    out.textContent = 'You scored ' + score + ' out of ' + names.length + ' ✓';
    out.style.color = (score === names.length) ? 'var(--green)' : '#0a0a0a';
  }
</script>

</body>
</html>

<!-- Chatbot Section -->
<style>
    /* Chatbot Floating Button */
    #chatbot-btn {
        position: fixed;
        bottom: 20px;
        right: 20px;
        background: #ffcb05;
        color: black;
        padding: 15px 20px;
        border-radius: 30px;
        cursor: pointer;
        font-weight: bold;
        border: 3px solid #ff6f6f;
        box-shadow: 0 0 10px #ff6f6f;
        animation: bounce 1.5s infinite;
    }

    /* Bounce animation */
    @keyframes bounce {
        0% { transform: translateY(0); }
        50% { transform: translateY(-8px); }
        100% { transform: translateY(0); }
    }

    /* Chat window */
    #chatbot-window {
        width: 320px;
        height: 420px;
        background: white;
        border-radius: 15px;
        position: fixed;
        bottom: 80px;
        right: 20px;
        border: 4px solid #ff6f6f;
        display: none;
        flex-direction: column;
        overflow: hidden;
    }

    #chat-header {
        background: #ffcb05;
        padding: 10px;
        font-size: 18px;
        font-weight: bold;
        text-align: center;
        border-bottom: 3px solid #ff6f6f;
    }

    #chat-body {
        flex: 1;
        padding: 10px;
        overflow-y: auto;
        font-size: 15px;
    }

    .bot-msg {
        background: #ffe5e5;
        padding: 8px;
        border-radius: 10px;
        margin-bottom: 8px;
    }

    .user-msg {
        background: #d7efff;
        padding: 8px;
        border-radius: 10px;
        margin-bottom: 8px;
        text-align: right;
    }

    #chat-input-area {
        display: flex;
        border-top: 2px solid #ddd;
    }

    #chat-input {
        flex: 1;
        padding: 10px;
        border: none;
        outline: none;
    }

    #send-btn {
        padding: 10px;
        background: #ff6f6f;
        color: white;
        border: none;
        cursor: pointer;
        font-weight: bold;
    }
</style>

<div id="chatbot-btn">🤖 Chat with Shinchan!</div>

<div id="chatbot-window">
    <div id="chat-header">Shinchan AI Helper</div>
    <div id="chat-body">
        <div class="bot-msg">Hi! I'm Shinchan! Ask me maths or anything fun 😁</div>
    </div>

    <div id="chat-input-area">
        <input id="chat-input" type="text" placeholder="Type your message...">
        <button id="send-btn">Send</button>
    </div>
</div>

<script>
    // Open / Close Chatbot
    document.getElementById("chatbot-btn").onclick = () => {
        const win = document.getElementById("chatbot-window");
        win.style.display = (win.style.display === "flex") ? "none" : "flex";
    };

    // Send Message
    document.getElementById("send-btn").onclick = sendMessage;
    document.getElementById("chat-input").addEventListener("keypress", function(e) {
        if (e.key === "Enter") sendMessage();
    });

    function sendMessage() {
        let input = document.getElementById("chat-input");
        let msg = input.value.trim();
        if (msg === "") return;

        addUser(msg);
        input.value = "";

        setTimeout(() => {
            addBot(botReply(msg));
        }, 400);
    }

    // Add user message
    function addUser(text) {
        let body = document.getElementById("chat-body");
        body.innerHTML += `<div class="user-msg">${text}</div>`;
        body.scrollTop = body.scrollHeight;
    }

    // Add bot message
    function addBot(text) {
        let body = document.getElementById("chat-body");
        body.innerHTML += `<div class="bot-msg">${text}</div>`;
        body.scrollTop = body.scrollHeight;
    }

    // Simple AI logic
    function botReply(message) {
        message = message.toLowerCase();

        // Math solving
        try {
            if (message.includes("+") || message.includes("-") ||
                message.includes("*") || message.includes("/")) {
                let ans = eval(message);
                return "Hehe! 🤓 The answer is: " + ans;
            }
        } catch { }

        // Custom replies
        if (message.includes("hi") || message.includes("hello"))
            return "Hiiii! I'm Shinchan! 😆";

        if (message.includes("your name"))
            return "I'm Shinchan, your math helper!";

        if (message.includes("bye"))
            return "Bye bye! See you soon! 👋";

        return "Ooops! I didn’t understand 😅 Ask me maths!";
    }
</script>
</a>
