# Melting-Maths-
Arithmetic learning site for Grades 1–10
<section class="bg-orange-100 py-6 mt-10">
  <div class="max-w-4xl mx-auto text-center">
    <h2 class="text-2xl text-orange-600 font-bold">👤 Co-Founder</h2>
    <p class="text-xl mt-2 text-gray-800">Laksh Agarwal</p>
  </div>
</section>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Grade 3 Quiz – Mealting Maths</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    body {
      font-family: 'Fredoka One', cursive;
    }
  </style>
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
   <h2 class="text-3xl text-center text-orange-500 mb-6
    <form id="quizForm" class="space-y-6">
      <div>
        <p class="font-semibold">1. What is 8 + 6?</p>
        <input type="radio" name="q1" value="12"> 12<br />
        <input type="radio" name="q1" value="13"> 13<br />
        <input type="radio" name="q1" value="14"> 14
      </div>

      <div>
        <p class="font-semibold">2. What is 24 ÷ 6?</p>
        <input type="radio" name="q2" value="3"> 3<br />
        <input type="radio" name="q2" value="4"> 4<br />
        <input type="radio" name="q2" value="6"> 6
      </div>

      <div>
        <p class="font-semibold">3. What is 7 × 3?</p>
        <input type="radio" name="q3" value="21"> 21<br />
        <input type="radio" name="q3" value="24"> 24<br />
        <input type="radio" name="q3" value="18"> 18
      </div>

      <div>
        <p class="font-semibold">4. What is the place value of 5 in 352?</p>
        <input type="radio" name="q4" value="5"> 5<br />
        <input type="radio" name="q4" value="50"> 50<br />
        <input type="radio" name="q4" value="500"> 500
      </div>

      <div>
        <p class="font-semibold">5. What is the smallest 3-digit number?</p>
        <input type="radio" name="q5" value="001"> 001<br />
        <input type="radio" name="q5" value="100"> 100<br />
        <input type="radio" name="q5" value="101"> 101
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
        q1: "14",
        q2: "4",
        q3: "21",
        q4: "50",
        q5: "100"
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
  <title>Grade 5 Quiz – Mealting Maths</title>
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
    <h2 class="text-3xl text-center text-orange-500 mb-6">Grade 5 Arithmetic Quiz</h2>

    <form id="quizForm" class="space-y-6">
      <div>
        <p class="font-semibold">1. What is 125 × 8?</p>
        <input type="radio" name="q1" value="1000"> 1000<br />
        <input type="radio" name="q1" value="1050"> 1050<br />
        <input type="radio" name="q1" value="1020"> 1020
      </div>

      <div>
        <p class="font-semibold">2. What is 625 ÷ 25?</p>
        <input type="radio" name="q2" value="25"> 25<br />
        <input type="radio" name="q2" value="20"> 20<br />
        <input type="radio" name="q2" value="15"> 15
      </div>

      <div>
        <p class="font-semibold">3. What is 1/4 + 3/4?</p>
        <input type="radio" name="q3" value="1"> 1<br />
        <input type="radio" name="q3" value="2"> 2<br />
        <input type="radio" name="q3" value="3/4"> 3/4
      </div>

      <div>
        <p class="font-semibold">4. What is 2.5 + 3.75?</p>
        <input type="radio" name="q4" value="6.25"> 6.25<br />
        <input type="radio" name="q4" value="5.5"> 5.5<br />
        <input type="radio" name="q4" value="7.5"> 7.5
      </div>

      <div>
        <p class="font-semibold">5. Ravi has 12 pencils. He gives 3 pencils to each of his 3 friends. How many pencils are left?</p>
        <input type="radio" name="q5" value="3"> 3<br />
        <input type="radio" name="q5" value="6"> 6<br />
        <input type="radio" name="q5" value="0"> 0
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
        q1: "1000",
        q2: "25",
        q3: "1",
        q4: "6.25",
        q5: "3"
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
