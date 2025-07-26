# Melting-Maths-
<section class="bg-orange-100 py-6 mt-10">
  <div class="max-w-4xl mx-auto text-center">
    <div class="text-center mt-8">
  <p class="mt-4 text-lg font-semibold text-gray-700">Laksh Agarwal<br><span class="text-sm text-gray-500">Co-Founder</span></p>
</div>
    <img src="laksh.jpg" alt="Co-Founder Laksh Agarwal" class="w-40 h-40 rounded-full mx-auto shadow-lg" />
    <h2 class="text-2xl text-orange-600 font-bold">👤 Co-Founder</h2>
    <p class="text-xl mt-2 text-gray-800">Laksh Agarwal</p>
  </div>
</section>

<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Grade X Arithmetic Quiz – Mealting Maths</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-blue-50 text-gray-800">
  <header class="bg-orange-400 p-4 shadow-md">
    <div class="max-w-6xl mx-auto flex justify-between items-center">
      <h1 class="text-3xl text-white">🍽 Mealting Maths</h1>
      <nav class="space-x-4 text-white">
        <a href="index.html" class="hover:underline">Home</a>
        <a href="quiz.html" class="hover:underline font-bold">Quizzes</a>
      </nav>
    </div>
  </header>
  <main class="max-w-3xl mx-auto mt-10 p-4">
    <div class="mb-6 text-center">
      <label for="gradeSelect" class="text-lg font-semibold text-gray-700 mr-2">Select Grade:</label>
      <select id="gradeSelect" class="p-2 rounded border border-gray-300" onchange="goToQuizPage()">
        <option disabled selected>Select a grade</option>
        <option value="quiz-grade1.html">Grade 1</option>
        <option value="quiz-grade2.html">Grade 2</option>
        <option value="quiz-grade3.html">Grade 3</option>
        <option value="quiz-grade4.html">Grade 4</option>
        <option value="quiz-grade5.html">Grade 5</option>
        <option value="quiz-grade6.html">Grade 6</option>
        <option value="quiz-grade7.html">Grade 7</option>
        <option value="quiz-grade8.html">Grade 8</option>
        <option value="quiz-grade9.html">Grade 9</option>
        <option value="quiz-grade10.html">Grade 10</option>
      </select>
    </div>
     <h2 class="text-3xl text-center text-orange-500 mb-6">Grade X Arithmetic Quiz</h2>
    <form id="quizForm" class="space-y-6">
      <!-- Replace these with grade-specific questions -->
      <div>
        <p class="font-semibold">1. Sample question?</p>
        <input type="radio" name="q1" value="A"> Option A<br />
        <input type="radio" name="q1" value="B"> Option B<br />
        <input type="radio" name="q1" value="C"> Option C
      </div>
      <div>
        <p class="font-semibold">2. Sample question?</p>
        <input type="radio" name="q2" value="A"> Option A<br />
        <input type="radio" name="q2" value="B"> Option B<br />
        <input type="radio" name="q2" value="C"> Option C
      </div>
      <div>
        <p class="font-semibold">3. Sample question?</p>
        <input type="radio" name="q3" value="A"> Option A<br />
        <input type="radio" name="q3" value="B"> Option B<br />
        <input type="radio" name="q3" value="C"> Option C
      </div>
      <div>
        <p class="font-semibold">4. Sample question?</p>
        <input type="radio" name="q4" value="A"> Option A<br />
        <input type="radio" name="q4" value="B"> Option B<br />
        <input type="radio" name="q4" value="C"> Option C
      </div>
      <div>
        <p class="font-semibold">5. Sample question?</p>
        <input type="radio" name="q5" value="A"> Option A<br />
        <input type="radio" name="q5" value="B"> Option B<br />
        <input type="radio" name="q5" value="C"> Option C
      </div>
      <button type="button" onclick="submitQuiz()" class="mt-4 bg-orange-400 hover:bg-orange-500 text-white font-bold py-2 px-6 rounded-xl">Submit</button>
    </form>
    <div id="result" class="mt-6 text-lg font-semibold text-green-600"></div>
  </main>

  <footer class="bg-orange-400 text-white text-center py-4 mt-10">
    <p>&copy; 2025 Mealting Maths. All rights reserved. 🧮</p>
  </footer>

  <script>
    function submitQuiz() {
      // Placeholder answers
      const correctAnswers = {
        q1: "A",
        q2: "B",
        q3: "C",
        q4: "A",
        q5: "C"
      };
      let score = 5;
      const form = document.forms["quizForm"];
      for (const key in correctAnswers) {
        if (form[key]?.value === correctAnswers[key]) {
          score++;
        }
      }
      document.getElementById("result").textContent = You scored ${score}/5!;
    }
    function goToQuizPage() {
      const selectedGrade = document.getElementById("gradeSelect").value;
      window.location.href = selectedGrade;
    }
  </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
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

 <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Grade 9 Quiz – Mealting Maths</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-blue-50 text-gray-800">
  <header class="bg-orange-400 p-4 shadow-md">
    <div class="max-w-6xl mx-auto flex justify-between items-center">
      <h1 class="text-3xl text-white">🍽️ Mealting Maths</h1>
      <nav class="space-x-4 text-white">
        <a href="index.html" class="hover:underline">Home</a>
        <a href="quiz.html" class="hover:underline font-bold">Quizzes</a>
      </nav>
    </div>
  </header>

  <main class="max-w-3xl mx-auto mt-10 p-4">
    <h2 class="text-3xl text-center text-orange-500 mb-6">Grade 9 Arithmetic Quiz – Advanced</h2>

    <form id="quizForm" class="space-y-6">
      <div>
        <p class="font-semibold">1. Simplify: 3² × 2³ − 4</p>
        <input type="radio" name="q1" value="68"> 68<br />
        <input type="radio" name="q1" value="20"> 20<br />
        <input type="radio" name="q1" value="68"> 68
      </div>

      <div>
        <p class="font-semibold">2. Solve: If 5x − 3 = 2x + 12, what is x?</p>
        <input type="radio" name="q2" value="5"> 5<br />
        <input type="radio" name="q2" value="6"> 6<br />
        <input type="radio" name="q2" value="7"> 7
      </div>

      <div>
        <p class="font-semibold">3. Find the value of: (3/4 ÷ 1/2) + (2/5 × 3/8)</p>
        <input type="radio" name="q3" value="2.3"> 2.3<br />
        <input type="radio" name="q3" value="2.05"> 2.05<br />
        <input type="radio" name="q3" value="2.1"> 2.1
      </div>

      <div>
        <p class="font-semibold">4. A number is increased by 30% and then decreased by 20%. What is the net percentage change?</p>
        <input type="radio" name="q4" value="4% increase"> 4% increase<br />
        <input type="radio" name="q4" value="10% increase"> 10% increase<br />
        <input type="radio" name="q4" value="4% decrease"> 4% decrease
      </div>

      <div>
        <p class="font-semibold">5. If (x − 3)(x + 5) = 0, what are the roots?</p>
        <input type="radio" name="q5" value="x = −5, 3"> x = −5, 3<br />
        <input type="radio" name="q5" value="x = 5, 3"> x = 5, 3<br />
        <input type="radio" name="q5" value="x = −3, 5"> x = −3, 5
      </div>

      <button type="button" onclick="submitQuiz()" class="mt-4 bg-orange-400 hover:bg-orange-500 text-white font-bold py-2 px-6 rounded-xl">Submit</button>
    </form>

    <div id="result" class="mt-6 text-lg font-semibold text-green-600"></div>
  </main>

  <footer class="bg-orange-400 text-white text-center py-4 mt-10">
    <p>&copy; 2025 Mealting Maths. All rights reserved. 🧮</p>
  </footer>

  <script>
    function submitQuiz() {
      const correctAnswers = {
        q1: "68",
        q2: "5",
        q3: "2.3",
        q4: "4% increase",
        q5: "x = −5, 3"
      };

      let score = 0;
      const form = document.forms["quizForm"];
      for (const key in correctAnswers) {
        if (form[key].value === correctAnswers[key]) {
          score++;
        }
      }

      document.getElementById("result").textContent = `You scored ${score}/5!`;
    }
  </script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Grade 10 Quiz – Mealting Maths</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-blue-50 text-gray-800">
  <header class="bg-orange-400 p-4 shadow-md">
    <div class="max-w-6xl mx-auto flex justify-between items-center">
      <h1 class="text-3xl text-white">🍽️ Mealting Maths</h1>
      <nav class="space-x-4 text-white">
        <a href="index.html" class="hover:underline">Home</a>
        <a href="quiz.html" class="hover:underline font-bold">Quizzes</a>
      </nav>
    </div>
  </header>

  <main class="max-w-3xl mx-auto mt-10 p-4">
    <h2 class="text-3xl text-center text-orange-500 mb-6">Grade 10 Arithmetic Quiz – Advanced</h2>

    <form id="quizForm" class="space-y-6">
      <div>
        <p class="font-semibold">1. Factorize: x² − 7x + 12</p>
        <input type="radio" name="q1" value="(x − 3)(x − 4)"> (x − 3)(x − 4)<br />
        <input type="radio" name="q1" value="(x + 3)(x − 4)"> (x + 3)(x − 4)<br />
        <input type="radio" name="q1" value="(x − 6)(x − 1)"> (x − 6)(x − 1)
      </div>

      <div>
        <p class="font-semibold">2. Solve: 3/(x+1) = 1/2</p>
        <input type="radio" name="q2" value="x = 5"> x = 5<br />
        <input type="radio" name="q2" value="x = 6"> x = 6<br />
        <input type="radio" name="q2" value="x = 3"> x = 3
      </div>

      <div>
        <p class="font-semibold">3. If the mean of 6 numbers is 12, what is their total sum?</p>
        <input type="radio" name="q3" value="60"> 60<br />
        <input type="radio" name="q3" value="72"> 72<br />
        <input type="radio" name="q3" value="66"> 66
      </div>

      <div>
        <p class="font-semibold">4. Simplify: (2x²y × 3xy²)</p>
        <input type="radio" name="q4" value="6x³y³"> 6x³y³<br />
        <input type="radio" name="q4" value="5x²y²"> 5x²y²<br />
        <input type="radio" name="q4" value="6x²y³"> 6x²y³
      </div>

      <div>
        <p class="font-semibold">5. Find the value of x: √(x + 9) = 5</p>
        <input type="radio" name="q5" value="x = 16"> x = 16<br />
        <input type="radio" name="q5" value="x = 25"> x = 25<br />
        <input type="radio" name="q5" value="x = 30"> x = 30
      </div>

      <button type="button" onclick="submitQuiz()" class="mt-4 bg-orange-400 hover:bg-orange-500 text-white font-bold py-2 px-6 rounded-xl">Submit</button>
    </form>

    <div id="result" class="mt-6 text-lg font-semibold text-green-600"></div>
  </main>

  <footer class="bg-orange-400 text-white text-center py-4 mt-10">
    <p>&copy; 2025 Mealting Maths. All rights reserved. 🧮</p>
  </footer>

  <script>
    function submitQuiz() {
      const correctAnswers = {
        q1: "(x − 3)(x − 4)",
        q2: "x = 5",
        q3: "72",
        q4: "6x³y³",
        q5: "x = 16"
      };

      let score = 0;
      const form = document.forms["quizForm"];
      for (const key in correctAnswers) {
        if (form[key].value === correctAnswers[key]) {
          score++;
        }
      }

      document.getElementById("result").textContent = `You scored ${score}/5!`;
    }
  </script>
</body>
</html>

      document.getElementById("result").textContent = `You scored ${score}/5!`;
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
