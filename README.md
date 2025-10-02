# Melting-Maths-
<section class="bg-orange-100 py-6 mt-10">
  <div class="max-w-4xl mx-auto text-center">
    <div class="text-center mt-8">
  <p class="mt-4 text-lg font-semibold text-gray-700">Laksh Agarwal<br><span class="text-sm text-gray-500">Founder</span></p>
</div>
    <img src="laksh.jpg" alt="Founder Laksh Agarwal" class="w-40 h-40 rounded-full mx-auto shadow-lg" />
    <h2 class="text-2xl text-orange-600 font-bold">👤 Co-Founder</h2>
    <p class="text-xl mt-2 text-gray-800">Laksh Agarwal</p>
  </div>
</section>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Select Grade | Arithmetic Quiz</title>
  <style>
    body {
    <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Melting Maths - Quiz Selector</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background: #f7faff;
    }
    header {
      background: #4CAF50;
      padding: 20px;
      text-align: center;
      color: white;
    }
    section {
      padding: 50px;
      border-bottom: 2px solid #ddd;
    }
    h2 {
      color: #2d2d86;
    }
    select, button {
      font-size: 18px;
      padding: 10px;
      margin: 10px;
    }
    button {
      background-color: #4CAF50;
      color: white;
      border: none;
      cursor: pointer;
    }
    button:hover {
      background-color: #45a049;
    }
  </style>
</head>
<body>

  <!-- Grade Selector -->
  <header>
    <h1>Welcome to Melting Maths 🎉</h1>
    <p>Select your grade to jump directly to your quiz 👇</p>
    <select id="gradeSelector">
      <option value="">-- Select Grade --</option>
      <option value="grade1quiz">Grade 1</option>
      <option value="grade2quiz">Grade 2</option>
      <option value="grade3quiz">Grade 3</option>
      <option value="grade4quiz">Grade 4</option>
      <option value="grade5quiz">Grade 5</option>
      <option value="grade6quiz">Grade 6</option>
      <option value="grade7quiz">Grade 7</option>
      <option value="grade8quiz">Grade 8</option>
      <option value="grade9quiz">Grade 9</option>
      <option value="grade10quiz">Grade 10</option>
    </select>
    <button onclick="goToGrade()">Go 🚀</button>
  </header>
   
 <section id="grade1quiz">
  <meta charset="UTF-8">
  <title>Grade 1 Arithmetic Quiz</title>
  <style>
    body {
      font-family: 'Comic Sans MS', sans-serif;
      background-color: #fffbe6;
      color: #333;
      padding: 20px;
    }
    h1 {
      color: #ff6600;
      text-align: center;
    }
    .question {
      margin: 20px 0;
      background-color: #f9f3d2;
      padding: 15px;
      border-radius: 12px;
      border: 2px solid #ffd966;
    }
    .question label {
      display: block;
      margin-bottom: 5px;
    }
    button {
      background-color: #4CAF50;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }
    #result {
      margin-top: 20px;
      font-size: 20px;
      font-weight: bold;
      color: #006600;
    }
  </style>
</head>
<body>

<h1>Grade 1 Arithmetic Quiz</h1>

<form id="quizForm">
  <div class="question">
    <label>1. What is 2 + 3?</label>
    <input type="radio" name="q1" value="4"> 4<br>
    <input type="radio" name="q1" value="5"> 5<br>
    <input type="radio" name="q1" value="6"> 6
  </div>

  <div class="question">
    <label>2. What is 7 - 4?</label>
    <input type="radio" name="q2" value="2"> 2<br>
    <input type="radio" name="q2" value="3"> 3<br>
    <input type="radio" name="q2" value="4"> 4
  </div>

  <div class="question">
    <label>3. What comes after 8?</label>
    <input type="radio" name="q3" value="9"> 9<br>
    <input type="radio" name="q3" value="7"> 7<br>
    <input type="radio" name="q3" value="6"> 6
  </div> 

  <div class="question">
    <label>4. What is 5 + 0?</label>
    <input type="radio" name="q4" value="5"> 5<br>
    <input type="radio" name="q4" value="0"> 0<br>
    <input type="radio" name="q4" value="1"> 1
  </div>

  <div class="question">
    <label>5. What is 10 - 5?</label>
    <input type="radio" name="q5" value="4"> 4<br>
    <input type="radio" name="q5" value="5"> 5<br>
    <input type="radio" name="q5" value="6"> 6
  </div>

  <button type="button" onclick="checkAnswers()">Submit</button>
</form>

<div id="result"></div>

<script>
  function checkAnswers() {
    let correct = 0;
    if (document.querySelector('input[name="q1"]:checked')?.value === "5") correct++;
    if (document.querySelector('input[name="q2"]:checked')?.value === "3") correct++;
    if (document.querySelector('input[name="q3"]:checked')?.value === "9") correct++;
    if (document.querySelector('input[name="q4"]:checked')?.value === "5") correct++;
    if (document.querySelector('input[name="q5"]:checked')?.value === "5") correct++;

    document.getElementById("result").textContent = 
      "You got " + correct + " out of 5 correct!";
  }
</script>

</body>
</html>

<section id="grade2quiz">
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Grade 2 Arithmetic Quiz</title>
  <style>
    body {
      background-color: #e0f7fa;
      font-family: 'Verdana', sans-serif;
      padding: 30px;
      text-align: center;
    }
    h1 {
      color: #00796b;
    }
    .question {
      background: #ffffff;
      border: 2px solid #4db6ac;
      padding: 20px;
      margin: 20px auto;
      border-radius: 10px;
      width: 90%;
      max-width: 600px;
      text-align: left;
    }
    input[type="radio"] {
      margin: 10px;
    }
    button {
      background-color: #00796b;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 6px;
      font-size: 16px;
      cursor: pointer;
      margin-top: 20px;
    }
    button:hover {
      background-color: #004d40;
    }
    #score {
      font-size: 20px;
      color: #1b5e20;
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <h1>Grade 2 Arithmetic Quiz</h1>

  <form id="quizForm">
    <div class="question">
      <p>1. What is 24 + 13?</p>
      <label><input type="radio" name="q1" value="a"> 37</label><br>
      <label><input type="radio" name="q1" value="b"> 36</label><br>
      <label><input type="radio" name="q1" value="c"> 38</label>
    </div>

    <div class="question">
      <p>2. What is the value of the digit 5 in 452?</p>
      <label><input type="radio" name="q2" value="a"> 500</label><br>
      <label><input type="radio" name="q2" value="b"> 50</label><br>
      <label><input type="radio" name="q2" value="c"> 5</label>
    </div>

    <div class="question">
      <p>3. Which number is greater?</p>
      <label><input type="radio" name="q3" value="a"> 98</label><br>
      <label><input type="radio" name="q3" value="b"> 89</label><br>
      <label><input type="radio" name="q3" value="c"> 88</label>
    </div>

    <div class="question">
      <p>4. What is 100 - 57?</p>
      <label><input type="radio" name="q4" value="a"> 53</label><br>
      <label><input type="radio" name="q4" value="b"> 43</label><br>
      <label><input type="radio" name="q4" value="c"> 47</label>
    </div>

    <div class="question">
      <p>5. Which number comes next: 10, 20, 30, ___?</p>
      <label><input type="radio" name="q5" value="a"> 35</label><br>
      <label><input type="radio" name="q5" value="b"> 40</label><br>
      <label><input type="radio" name="q5" value="c"> 50</label>
    </div>

    <button type="button" onclick="checkAnswers()">Submit</button>
    <div id="score"></div>
  </form>

  <script>
    function checkAnswers() {
      let score = 0;
      const answers = {
        q1: 'a',
        q2: 'b',
        q3: 'a',
        q4: 'b',
        q5: 'b'
      };

      for (let q in answers) {
        const selected = document.querySelector('input[name=' + q + ']:checked');
        if (selected && selected.value === answers[q]) {
          score++;
        }
      }

      document.getElementById("score").innerText = "You scored " + score + " out of 5!";
    }
  </script>
</body>
</html>

<section id="grade3quiz">
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Grade 3 Arithmetic Quiz</title>
  <style>
    body {
      background-color: #fff8e1;
      font-family: 'Segoe UI', sans-serif;
      padding: 30px;
      text-align: center;
    }
    h1 {
      color: #ef6c00;
    }
    .question {
      background: #ffffff;
      border: 2px solid #ffb74d;
      padding: 20px;
      margin: 20px auto;
      border-radius: 10px;
      width: 90%;
      max-width: 600px;
      text-align: left;
    }
    input[type="radio"] {
      margin: 10px;
    }
    button {
      background-color: #ef6c00;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 6px;
      font-size: 16px;
      cursor: pointer;
      margin-top: 20px;
    }
    button:hover {
      background-color: #e65100;
    }
    #score {
      font-size: 20px;
      color: #2e7d32;
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <h1>Grade 3 Arithmetic Quiz</h1>

  <form id="quizForm">
    <div class="question">
      <p>1. What is 45 ÷ 5?</p>
      <label><input type="radio" name="q1" value="a"> 9</label><br>
      <label><input type="radio" name="q1" value="b"> 8</label><br>
      <label><input type="radio" name="q1" value="c"> 10</label>
    </div>

    <div class="question">
      <p>2. What is the sum of 345 and 276?</p>
      <label><input type="radio" name="q2" value="a"> 621</label><br>
      <label><input type="radio" name="q2" value="b"> 611</label><br>
      <label><input type="radio" name="q2" value="c"> 620</label>
    </div>

    <div class="question">
      <p>3. What is 100 less than 953?</p>
      <label><input type="radio" name="q3" value="a"> 863</label><br>
      <label><input type="radio" name="q3" value="b"> 853</label><br>
      <label><input type="radio" name="q3" value="c"> 843</label>
    </div>

    <div class="question">
      <p>4. Multiply: 7 × 8</p>
      <label><input type="radio" name="q4" value="a"> 54</label><br>
      <label><input type="radio" name="q4" value="b"> 56</label><br>
      <label><input type="radio" name="q4" value="c"> 64</label>
    </div>

    <div class="question">
      <p>5. What is the place value of 2 in 524?</p>
      <label><input type="radio" name="q5" value="a"> 2</label><br>
      <label><input type="radio" name="q5" value="b"> 20</label><br>
      <label><input type="radio" name="q5" value="c"> 200</label>
    </div>

    <button type="button" onclick="checkAnswers()">Submit</button>
    <div id="score"></div>
  </form>

  <script>
    function checkAnswers() {
      let score = 0;
      const answers = {
        q1: 'a',
        q2: 'a',
        q3: 'b',
        q4: 'b',
        q5: 'b'
      };

      for (let q in answers) {
        const selected = document.querySelector('input[name=' + q + ']:checked');
        if (selected && selected.value === answers[q]) {
          score++;
        }
      }

      document.getElementById("score").innerText = "You scored " + score + " out of 5!";
    }
  </script>
</body>
</html>

<section id="grade4quiz">
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Grade 4 Arithmetic Quiz</title>
  <style>
    body {
      background-color: #e1f5fe;
      font-family: 'Segoe UI', sans-serif;
      padding: 30px;
      text-align: center;
    }
    h1 {
      color: #0277bd;
    }
    .question {
      background: #ffffff;
      border: 2px solid #4fc3f7;
      padding: 20px;
      margin: 20px auto;
      border-radius: 10px;
      width: 90%;
      max-width: 600px;
      text-align: left;
    }
    input[type="radio"] {
      margin: 10px;
    }
    button {
      background-color: #0288d1;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 6px;
      font-size: 16px;
      cursor: pointer;
      margin-top: 20px;
    }
    button:hover {
      background-color: #01579b;
    }
    #score {
      font-size: 20px;
      color: #2e7d32;
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <h1>Grade 4 Arithmetic Quiz</h1>

  <form id="quizForm">
    <div class="question">
      <p>1. What is the product of 23 × 4?</p>
      <label><input type="radio" name="q1" value="a"> 82</label><br>
      <label><input type="radio" name="q1" value="b"> 92</label><br>
      <label><input type="radio" name="q1" value="c"> 86</label>
    </div>

    <div class="question">
      <p>2. What is the value of 378 + 245?</p>
      <label><input type="radio" name="q2" value="a"> 623</label><br>
      <label><input type="radio" name="q2" value="b"> 613</label><br>
      <label><input type="radio" name="q2" value="c"> 633</label>
    </div>

    <div class="question">
      <p>3. What is 1000 - 475?</p>
      <label><input type="radio" name="q3" value="a"> 525</label><br>
      <label><input type="radio" name="q3" value="b"> 535</label><br>
      <label><input type="radio" name="q3" value="c"> 545</label>
    </div>

    <div class="question">
      <p>4. Which of the following is a multiple of 9?</p>
      <label><input type="radio" name="q4" value="a"> 27</label><br>
      <label><input type="radio" name="q4" value="b"> 26</label><br>
      <label><input type="radio" name="q4" value="c"> 25</label>
    </div>

    <div class="question">
      <p>5. What is the place value of 6 in the number 763?</p>
      <label><input type="radio" name="q5" value="a"> 60</label><br>
      <label><input type="radio" name="q5" value="b"> 600</label><br>
      <label><input type="radio" name="q5" value="c"> 6</label>
    </div>

    <button type="button" onclick="checkAnswers()">Submit</button>
    <div id="score"></div>
  </form>

  <script>
    function checkAnswers() {
      let score = 0;
      const answers = {
        q1: 'b',
        q2: 'a',
        q3: 'a',
        q4: 'a',
        q5: 'a'
      };

      for (let q in answers) {
        const selected = document.querySelector('input[name=' + q + ']:checked');
        if (selected && selected.value === answers[q]) {
          score++;
        }
      }

      document.getElementById("score").innerText = "You scored " + score + " out of 5!";
    }
  </script>
</body>
</html>

 <section id="grade5quiz">
 <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Grade 5 Arithmetic Quiz</title>
  <style>
    body {
      background-color: #fff3e0;
      font-family: 'Segoe UI', sans-serif;
      padding: 30px;
      text-align: center;
    }
    h1 {
      color: #ef6c00;
    }
    .question {
      background: #ffffff;
      border: 2px solid #ffb74d;
      padding: 20px;
      margin: 20px auto;
      border-radius: 10px;
      width: 90%;
      max-width: 600px;
      text-align: left;
    }
    input[type="radio"] {
      margin: 10px;
    }
    button {
      background-color: #fb8c00;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 6px;
      font-size: 16px;
      cursor: pointer;
      margin-top: 20px;
    }
    button:hover {
      background-color: #e65100;
    }
    #score {
      font-size: 20px;
      color: #2e7d32;
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <h1>Grade 5 Arithmetic Quiz</h1>

  <form id="quizForm">
    <div class="question">
      <p>1. What is the LCM of 12 and 18?</p>
      <label><input type="radio" name="q1" value="a"> 36</label><br>
      <label><input type="radio" name="q1" value="b"> 24</label><br>
      <label><input type="radio" name="q1" value="c"> 6</label>
    </div>

    <div class="question">
      <p>2. Simplify: (48 ÷ 4) + (5 × 2)</p>
      <label><input type="radio" name="q2" value="a"> 22</label><br>
      <label><input type="radio" name="q2" value="b"> 23</label><br>
      <label><input type="radio" name="q2" value="c"> 21</label>
    </div>

    <div class="question">
      <p>3. What is 35% of 200?</p>
      <label><input type="radio" name="q3" value="a"> 65</label><br>
      <label><input type="radio" name="q3" value="b"> 70</label><br>
      <label><input type="radio" name="q3" value="c"> 75</label>
    </div>

    <div class="question">
      <p>4. What is the value of 6² + 4²?</p>
      <label><input type="radio" name="q4" value="a"> 52</label><br>
      <label><input type="radio" name="q4" value="b"> 50</label><br>
      <label><input type="radio" name="q4" value="c"> 48</label>
    </div>

    <div class="question">
      <p>5. Round 4867 to the nearest hundred:</p>
      <label><input type="radio" name="q5" value="a"> 4900</label><br>
      <label><input type="radio" name="q5" value="b"> 4800</label><br>
      <label><input type="radio" name="q5" value="c"> 5000</label>
    </div>

    <button type="button" onclick="checkAnswers()">Submit</button>
    <div id="score"></div>
  </form>

  <script>
    function checkAnswers() {
      let score = 0;
      const answers = {
        q1: 'a',
        q2: 'c',
        q3: 'b',
        q4: 'a',
        q5: 'a'
      };

      for (let q in answers) {
        const selected = document.querySelector('input[name=' + q + ']:checked');
        if (selected && selected.value === answers[q]) {
          score++;
        }
      }

      document.getElementById("score").innerText = "You scored " + score + " out of 5!";
    }
  </script>
</body>
</html>

<section id="grade6quiz">
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Grade 6 Arithmetic Quiz</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background-color: #f4f6f9;
      padding: 20px;
    }
    .quiz-container {
      max-width: 800px;
      margin: auto;
      background: white;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    h1 {
      text-align: center;
      color: #2c3e50;
    }
    .question {
      margin: 20px 0;
    }
    .question p {
      font-weight: bold;
    }
    label {
      display: block;
      margin-left: 20px;
      margin-bottom: 5px;
    }
    button {
      background-color: #3498db;
      color: white;
      padding: 10px 20px;
      font-size: 16px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }
    #result {
      margin-top: 20px;
      font-size: 18px;
      font-weight: bold;
      color: green;
    }
  </style>
</head>
<body>

  <div class="quiz-container">
    <h1>Grade 6 Arithmetic Quiz (MCQs)</h1>
    <form id="quizForm">

      <div class="question">
        <p>1. What is the value of 7 × (4 + 2)?</p>
        <label><input type="radio" name="q1" value="42"> 42</label>
        <label><input type="radio" name="q1" value="28"> 28</label>
        <label><input type="radio" name="q1" value="46"> 46</label>
        <label><input type="radio" name="q1" value="48"> 48</label>
      </div>

      <div class="question">
        <p>2. Find the LCM of 6 and 8.</p>
        <label><input type="radio" name="q2" value="24"> 24</label>
        <label><input type="radio" name="q2" value="14"> 14</label>
        <label><input type="radio" name="q2" value="48"> 48</label>
        <label><input type="radio" name="q2" value="18"> 18</label>
      </div>

      <div class="question">
        <p>3. If 35 ÷ 7 = 5, what is 7 × 5?</p>
        <label><input type="radio" name="q3" value="40"> 40</label>
        <label><input type="radio" name="q3" value="35"> 35</label>
        <label><input type="radio" name="q3" value="25"> 25</label>
        <label><input type="radio" name="q3" value="30"> 30</label>
      </div>

      <div class="question">
        <p>4. Which of these numbers is a prime number?</p>
        <label><input type="radio" name="q4" value="21"> 21</label>
        <label><input type="radio" name="q4" value="17"> 17</label>
        <label><input type="radio" name="q4" value="27"> 27</label>
        <label><input type="radio" name="q4" value="49"> 49</label>
      </div>

      <div class="question">
        <p>5. What is the area of a square with side 9 cm?</p>
        <label><input type="radio" name="q5" value="81"> 81 cm²</label>
        <label><input type="radio" name="q5" value="18"> 18 cm²</label>
        <label><input type="radio" name="q5" value="72"> 72 cm²</label>
        <label><input type="radio" name="q5" value="90"> 90 cm²</label>
      </div>

      <button type="button" onclick="checkAnswers()">Submit</button>
    </form>
    <div id="result"></div>
  </div>

  <script>
    function checkAnswers() {
      const answers = {
        q1: "42",
        q2: "24",
        q3: "35",
        q4: "17",
        q5: "81"
      };

      let score = 0;
      for (let key in answers) {
        const selected = document.querySelector('input[name="' + key + '"]:checked');
        if (selected && selected.value === answers[key]) {
          score++;
        }
      }

      document.getElementById("result").innerText = "You scored " + score + " out of 5!";
    }
  </script>
</body>
</html>

<section id="grade7quiz">
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Grade 7 Arithmetic Quiz – Test Your Skills!</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #fefae0;
      padding: 20px;
      margin: 0;
      color: #333;
    }
    h1 {
      text-align: center;
      color: #283618;
      margin-bottom: 30px;
    }
    .quiz-container {
      max-width: 700px;
      margin: auto;
      background-color: #d8f3dc;
      border-radius: 10px;
      padding: 20px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }
    .question {
      margin-bottom: 20px;
    }
    .question h3 {
      margin-bottom: 10px;
    }
    input[type="radio"] {
      margin-right: 10px;
    }
    #submit {
      background-color: #606c38;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    #result {
      margin-top: 20px;
      font-weight: bold;
      font-size: 18px;
      color: #2a9d8f;
    }
  </style>
</head>
<body>
  <div class="quiz-container">
    <h1>Grade 7 Arithmetic Quiz – Test Your Skills!</h1>

    <form id="quizForm">
      <div class="question">
        <h3>1. What is the value of 7² - 3²?</h3>
        <label><input type="radio" name="q1" value="a"> 40</label><br />
        <label><input type="radio" name="q1" value="b"> 49</label><br />
        <label><input type="radio" name="q1" value="c"> 16</label><br />
        <label><input type="radio" name="q1" value="d"> 30</label>
      </div>

      <div class="question">
        <h3>2. What is the reciprocal of 5/8?</h3>
        <label><input type="radio" name="q2" value="a"> 8/5</label><br />
        <label><input type="radio" name="q2" value="b"> -5/8</label><br />
        <label><input type="radio" name="q2" value="c"> 13/8</label><br />
        <label><input type="radio" name="q2" value="d"> 3/5</label>
      </div>

      <div class="question">
        <h3>3. Find the value of: (2 + 3) × 4</h3>
        <label><input type="radio" name="q3" value="a"> 20</label><br />
        <label><input type="radio" name="q3" value="b"> 14</label><br />
        <label><input type="radio" name="q3" value="c"> 24</label><br />
        <label><input type="radio" name="q3" value="d"> 10</label>
      </div>

      <div class="question">
        <h3>4. What is 25% of 160?</h3>
        <label><input type="radio" name="q4" value="a"> 40</label><br />
        <label><input type="radio" name="q4" value="b"> 35</label><br />
        <label><input type="radio" name="q4" value="c"> 45</label><br />
        <label><input type="radio" name="q4" value="d"> 32</label>
      </div>

      <div class="question">
        <h3>5. If 12 pens cost ₹144, what is the cost of 5 pens?</h3>
        <label><input type="radio" name="q5" value="a"> ₹50</label><br />
        <label><input type="radio" name="q5" value="b"> ₹60</label><br />
        <label><input type="radio" name="q5" value="c"> ₹70</label><br />
        <label><input type="radio" name="q5" value="d"> ₹72</label>
      </div>

      <button type="button" id="submit" onclick="calculateScore()">Submit</button>
    </form>

    <div id="result"></div>
  </div>

  <script>
    function calculateScore() {
      const answers = {
        q1: "a",
        q2: "a",
        q3: "a",
        q4: "a",
        q5: "d"
      };
      let score = 0;

      for (let key in answers) {
        const selected = document.querySelector(`input[name="${key}"]:checked`);
        if (selected && selected.value === answers[key]) {
          score++;
        }
      }

      document.getElementById("result").innerText = `Your score: ${score} out of 5`;
    }
  </script>
</body>
</html>

<section id="grade8quiz">
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Grade 8 Arithmetic Quiz – Challenge Your Brain!</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      background-color: #f9f9ff;
      padding: 20px;
      margin: 0;
      color: #333;
    }
    h1 {
      text-align: center;
      color: #1d3557;
      margin-bottom: 30px;
    }
    .quiz-container {
      max-width: 700px;
      margin: auto;
      background-color: #e0f7fa;
      border-radius: 10px;
      padding: 20px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }
    .question {
      margin-bottom: 20px;
    }
    .question h3 {
      margin-bottom: 10px;
    }
    input[type="radio"] {
      margin-right: 10px;
    }
    #submit {
      background-color: #0077b6;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    #result {
      margin-top: 20px;
      font-weight: bold;
      font-size: 18px;
      color: #2e7d32;
    }
  </style>
</head>
<body>
  <div class="quiz-container">
    <h1>Grade 8 Arithmetic Quiz – Challenge Your Brain!</h1>

    <form id="quizForm">
      <div class="question">
        <h3>1. Simplify: (4x - 3)²</h3>
        <label><input type="radio" name="q1" value="a"> 16x² - 24x + 9</label><br />
        <label><input type="radio" name="q1" value="b"> 16x² - 9</label><br />
        <label><input type="radio" name="q1" value="c"> 4x² - 9</label><br />
        <label><input type="radio" name="q1" value="d"> None of these</label>
      </div>

      <div class="question">
        <h3>2. If the ratio of boys to girls is 3:5, what percent of the class are girls?</h3>
        <label><input type="radio" name="q2" value="a"> 60%</label><br />
        <label><input type="radio" name="q2" value="b"> 62.5%</label><br />
        <label><input type="radio" name="q2" value="c"> 40%</label><br />
        <label><input type="radio" name="q2" value="d"> 70%</label>
      </div>

      <div class="question">
        <h3>3. Solve: 3/4 + 2/3 = ?</h3>
        <label><input type="radio" name="q3" value="a"> 17/12</label><br />
        <label><input type="radio" name="q3" value="b"> 6/7</label><br />
        <label><input type="radio" name="q3" value="c"> 5/7</label><br />
        <label><input type="radio" name="q3" value="d"> 11/12</label>
      </div>

      <div class="question">
        <h3>4. A number is increased by 20% and then decreased by 20%. What is the net change?</h3>
        <label><input type="radio" name="q4" value="a"> No change</label><br />
        <label><input type="radio" name="q4" value="b"> Increase 4%</label><br />
        <label><input type="radio" name="q4" value="c"> Decrease 4%</label><br />
        <label><input type="radio" name="q4" value="d"> Increase 20%</label>
      </div>

      <div class="question">
        <h3>5. The square root of 324 is:</h3>
        <label><input type="radio" name="q5" value="a"> 18</label><br />
        <label><input type="radio" name="q5" value="b"> 17</label><br />
        <label><input type="radio" name="q5" value="c"> 19</label><br />
        <label><input type="radio" name="q5" value="d"> 16</label>
      </div>

      <button type="button" id="submit" onclick="calculateScore()">Submit</button>
    </form>

    <div id="result"></div>
  </div>

  <script>
    function calculateScore() {
      const answers = {
        q1: "a",
        q2: "b",
        q3: "a",
        q4: "c",
        q5: "a"
      };
      let score = 0;

      for (let key in answers) {
        const selected = document.querySelector(`input[name="${key}"]:checked`);
        if (selected && selected.value === answers[key]) {
          score++;
        }
      }

      document.getElementById("result").innerText = `Your score: ${score} out of 5`;
    }
  </script>
</body>
</html>

<section id="grade9quiz">
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Grade 9 Arithmetic Quiz – Test Your Logical Power!</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background-color: #f2f2f2;
      padding: 20px;
      margin: 0;
      color: #333;
    }
    h1 {
      text-align: center;
      color: #2b2d42;
      margin-bottom: 30px;
    }
    .quiz-container {
      max-width: 700px;
      margin: auto;
      background-color: #ffffff;
      border-radius: 10px;
      padding: 25px;
      box-shadow: 0 5px 12px rgba(0, 0, 0, 0.1);
    }
    .question {
      margin-bottom: 20px;
    }
    .question h3 {
      margin-bottom: 10px;
    }
    input[type="radio"] {
      margin-right: 8px;
    }
    #submit {
      background-color: #0077b6;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 6px;
      cursor: pointer;
    }
    #result {
      margin-top: 20px;
      font-weight: bold;
      font-size: 18px;
      color: #007f5f;
    }
  </style>
</head>
<body>
  <div class="quiz-container">
    <h1>Grade 9 Arithmetic Quiz – Test Your Logical Power!</h1>

    <form id="quizForm">
      <div class="question">
        <h3>1. If x² + 5x + 6 = 0, what are the roots of the equation?</h3>
        <label><input type="radio" name="q1" value="a"> x = -2, x = -3</label><br />
        <label><input type="radio" name="q1" value="b"> x = 2, x = 3</label><br />
        <label><input type="radio" name="q1" value="c"> x = -1, x = -6</label><br />
        <label><input type="radio" name="q1" value="d"> x = 1, x = 6</label>
      </div>

      <div class="question">
        <h3>2. Evaluate: (3² × 2³) ÷ 6</h3>
        <label><input type="radio" name="q2" value="a"> 8</label><br />
        <label><input type="radio" name="q2" value="b"> 6</label><br />
        <label><input type="radio" name="q2" value="c"> 12</label><br />
        <label><input type="radio" name="q2" value="d"> 9</label>
      </div>

      <div class="question">
        <h3>3. A man’s salary is increased by 10% and then decreased by 10%. What is the net change?</h3>
        <label><input type="radio" name="q3" value="a"> Increase by 1%</label><br />
        <label><input type="radio" name="q3" value="b"> No change</label><br />
        <label><input type="radio" name="q3" value="c"> Decrease by 1%</label><br />
        <label><input type="radio" name="q3" value="d"> Decrease by 10%</label>
      </div>

      <div class="question">
        <h3>4. If √x = 7, what is the value of x + √x?</h3>
        <label><input type="radio" name="q4" value="a"> 56</label><br />
        <label><input type="radio" name="q4" value="b"> 57</label><br />
        <label><input type="radio" name="q4" value="c"> 49</label><br />
        <label><input type="radio" name="q4" value="d"> 14</label>
      </div>

      <div class="question">
        <h3>5. Simplify: (2x + 3)(2x - 3)</h3>
        <label><input type="radio" name="q5" value="a"> 4x² + 9</label><br />
        <label><input type="radio" name="q5" value="b"> 4x² - 9</label><br />
        <label><input type="radio" name="q5" value="c"> 4x² + 6x - 9</label><br />
        <label><input type="radio" name="q5" value="d"> 4x² - 6x - 9</label>
      </div>

      <button type="button" id="submit" onclick="calculateScore()">Submit</button>
    </form>

    <div id="result"></div>
  </div>

  <script>
    function calculateScore() {
      const answers = {
        q1: "a",
        q2: "b",
        q3: "c",
        q4: "b",
        q5: "b"
      };
      let score = 0;

      for (let key in answers) {
        const selected = document.querySelector(`input[name="${key}"]:checked`);
        if (selected && selected.value === answers[key]) {
          score++;
        }
      }

      document.getElementById("result").innerText = `Your score: ${score} out of 5`;
    }
  </script>
</body>
</html>

<section id="grade10quiz">
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Grade 10 Arithmetic Quiz</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      background-color: #fef6e4;
      color: #333;
      padding: 20px;
      max-width: 700px;
      margin: auto;
      border: 2px solid #ffcb77;
      border-radius: 20px;
      box-shadow: 0 0 20px #ffc300;
    }
    h1 {
      text-align: center;
      color: #ff6f61;
    }
    .question {
      margin: 20px 0;
    }
    .question label {
      display: block;
      margin: 5px 0;
    }
    button {
      background-color: #ff6f61;
      color: white;
      padding: 10px 20px;
      border: none;
      margin-top: 20px;
      border-radius: 10px;
      font-size: 16px;
    }
    #result {
      margin-top: 20px;
      font-size: 18px;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1>Grade 10 Arithmetic Quiz – Final Boss Level!</h1>
  <form id="quizForm">
    <div class="question">
      <p>1. If x² – 9x + 20 = 0, what are the roots?</p>
      <label><input type="radio" name="q1" value="a"> x = 4 or x = 5</label>
      <label><input type="radio" name="q1" value="b"> x = 2 or x = 10</label>
      <label><input type="radio" name="q1" value="c"> x = -4 or x = -5</label>
      <label><input type="radio" name="q1" value="d"> x = 3 or x = 6</label>
    </div>

    <div class="question">
      <p>2. Evaluate: (2/3) ÷ (4/9)</p>
      <label><input type="radio" name="q2" value="a"> 3/2</label>
      <label><input type="radio" name="q2" value="b"> 2/3</label>
      <label><input type="radio" name="q2" value="c"> 9/8</label>
      <label><input type="radio" name="q2" value="d"> 3/4</label>
    </div>

    <div class="question">
      <p>3. Simplify: (x - 2)(x + 2)</p>
      <label><input type="radio" name="q3" value="a"> x² - 4</label>
      <label><input type="radio" name="q3" value="b"> x² + 4</label>
      <label><input type="radio" name="q3" value="c"> x² - 2</label>
      <label><input type="radio" name="q3" value="d"> x² + 2</label>
    </div>

    <div class="question">
      <p>4. A train travels 120 km in 2 hours. What is its speed in m/s?</p>
      <label><input type="radio" name="q4" value="a"> 16.67 m/s</label>
      <label><input type="radio" name="q4" value="b"> 60 m/s</label>
      <label><input type="radio" name="q4" value="c"> 30 m/s</label>
      <label><input type="radio" name="q4" value="d"> 40 m/s</label>
    </div>

    <div class="question">
      <p>5. The sum of interior angles of a hexagon is:</p>
      <label><input type="radio" name="q5" value="a"> 720°</label>
      <label><input type="radio" name="q5" value="b"> 540°</label>
      <label><input type="radio" name="q5" value="c"> 600°</label>
      <label><input type="radio" name="q5" value="d"> 900°</label>
    </div>

    <button type="button" onclick="checkAnswers()">Submit</button>
    <div id="result"></div>
  </form>

  <script>
    function checkAnswers() {
      const answers = {
        q1: "a",
        q2: "a",
        q3: "a",
        q4: "a",
        q5: "a"
      };
      let score = 0;
      for (let q in answers) {
        const selected = document.querySelector(`input[name="${q}"]:checked`);
        if (selected && selected.value === answers[q]) {
          score++;
        }
      }
      document.getElementById("result").innerText =
        "Your score is " + score + " out of 5.";
    }
  </script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Mealting Maths – Feedback</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background-color: #fef6e4;
      margin: 0;
      padding: 0;
    }
    .container {
      max-width: 900px;
      margin: 40px auto;
      background: #fff;
      border-radius: 20px;
      box-shadow: 0 8px 16px rgba(0,0,0,0.1);
      padding: 20px;
    }
    h1 {
      text-align: center;
      color: #ff6f3c;
    }
    iframe {
      width: 100%;
      height: 900px;
      border: none;
      border-radius: 10px;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>We Value Your Feedback!</h1>
    <iframe 
      src="https://docs.google.com/forms/d/e/1FAIpQLSf8zt6PB5Fz2ZlhWNwRFdu_ED9dGMgbzNrli7twqx-nB0AlVA/viewform?embedded=true" 
      frameborder="0" 
      marginheight="0" 
      marginwidth="0"
      loading="lazy">
      Loading…
    </iframe>
  </div>
</body>
</html>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>About Us - Mealting Maths</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #fff8e7;
            color: #333;
            margin: 0;
            padding: 20px;
        }
        .container {
            max-width: 900px;
            margin: auto;
            background: #ffffff;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 0 15px rgba(0,0,0,0.1);
        }
        h1 {
            color: #e67e22;
            text-align: center;
        }
        h2 {
            color: #3498db;
        }
        p {
            font-size: 18px;
            line-height: 1.6;
        }
        .highlight {
            color: #2ecc71;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>About Us</h1>
        <h2>✨ Meet the Founder</h2>
        <p>
            Hi! I'm <span class="highlight">Laksh Agarwal</span>, a Grade 7 student from <span class="highlight">India</span>. I’m the founder of <strong>Mealting Maths</strong> — a free educational website built especially for students from <strong>Grade 1 to 10</strong>. I created this platform because I truly believe that maths doesn’t have to be scary or boring. With colorful quizzes and simple design, learning numbers can actually be fun!
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

