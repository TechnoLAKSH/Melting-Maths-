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
GRADE 1 ARTHMATIC QUIZ
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

      let score = 5;
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
 <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Grade 2 Quiz – Mealting Maths</title>
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
    <h2 class="text-3xl text-center text-orange-500 mb-6">Grade 2 Arithmetic Quiz</h2>

    <form id="quizForm" class="space-y-6">
      <div>
        <p class="font-semibold">1. What is 6 + 7?</p>
        <input type="radio" name="q1" value="12"> 12<br />
        <input type="radio" name="q1" value="13"> 13<br />
        <input type="radio" name="q1" value="14"> 14
      </div>

      <div>
        <p class="font-semibold">2. What is 15 - 8?</p>
        <input type="radio" name="q2" value="6"> 6<br />
        <input type="radio" name="q2" value="7"> 7<br />
        <input type="radio" name="q2" value="8"> 8
      </div>

      <div>
        <p class="font-semibold">3. What number comes after 49?</p>
        <input type="radio" name="q3" value="48"> 48<br />
        <input type="radio" name="q3" value="50"> 50<br />
        <input type="radio" name="q3" value="51"> 51
      </div>

      <div>
        <p class="font-semibold">4. What is 5 × 2?</p>
        <input type="radio" name="q4" value="10"> 10<br />
        <input type="radio" name="q4" value="7"> 7<br />
        <input type="radio" name="q4" value="12"> 12
      </div>

      <div>
        <p class="font-semibold">5. What is 20 ÷ 5?</p>
        <input type="radio" name="q5" value="3"> 3<br />
        <input type="radio" name="q5" value="4"> 4<br />
        <input type="radio" name="q5" value="5"> 5
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
        q1: "13",
        q2: "7",
        q3: "50",
        q4: "10",
        q5: "4"
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
  <title>Grade 3 Quiz – Mealting Maths</title>
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
    <h2 class="text-3xl text-center text-orange-500 mb-6">Grade 3 Arithmetic Quiz</h2>

    <form id="quizForm" class="space-y-6">
      <div>
        <p class="font-semibold">1. What is 23 + 19?</p>
        <input type="radio" name="q1" value="42"> 42<br />
        <input type="radio" name="q1" value="43"> 43<br />
        <input type="radio" name="q1" value="44"> 44
      </div>

      <div>
        <p class="font-semibold">2. What is 50 - 17?</p>
        <input type="radio" name="q2" value="33"> 33<br />
        <input type="radio" name="q2" value="32"> 32<br />
        <input type="radio" name="q2" value="34"> 34
      </div>

      <div>
        <p class="font-semibold">3. What is 6 × 4?</p>
        <input type="radio" name="q3" value="24"> 24<br />
        <input type="radio" name="q3" value="20"> 20<br />
        <input type="radio" name="q3" value="26"> 26
      </div>

      <div>
        <p class="font-semibold">4. What is 36 ÷ 6?</p>
        <input type="radio" name="q4" value="5"> 5<br />
        <input type="radio" name="q4" value="6"> 6<br />
        <input type="radio" name="q4" value="7"> 7
      </div>

      <div>
        <p class="font-semibold">5. I had 5 candies. I bought 3 more packs with 2 candies each. How many do I have now?</p>
        <input type="radio" name="q5" value="9"> 9<br />
        <input type="radio" name="q5" value="10"> 10<br />
        <input type="radio" name="q5" value="11"> 11
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
        q1: "42",
        q2: "33",
        q3: "24",
        q4: "6",
        q5: "11"
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
  <title>Grade 4 Quiz – Mealting Maths</title>
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
    <h2 class="text-3xl text-center text-orange-500 mb-6">Grade 4 Arithmetic Quiz</h2>

    <form id="quizForm" class="space-y-6">
      <div>
        <p class="font-semibold">1. What is 125 + 378?</p>
        <input type="radio" name="q1" value="493"> 493<br />
        <input type="radio" name="q1" value="503"> 503<br />
        <input type="radio" name="q1" value="513"> 513
      </div>

      <div>
        <p class="font-semibold">2. What is 900 - 475?</p>
        <input type="radio" name="q2" value="425"> 425<br />
        <input type="radio" name="q2" value="435"> 435<br />
        <input type="radio" name="q2" value="445"> 445
      </div>

      <div>
        <p class="font-semibold">3. What is 12 × 6?</p>
        <input type="radio" name="q3" value="72"> 72<br />
        <input type="radio" name="q3" value="76"> 76<br />
        <input type="radio" name="q3" value="66"> 66
      </div>

      <div>
        <p class="font-semibold">4. What is 144 ÷ 12?</p>
        <input type="radio" name="q4" value="11"> 11<br />
        <input type="radio" name="q4" value="12"> 12<br />
        <input type="radio" name="q4" value="13"> 13
      </div>

      <div>
        <p class="font-semibold">5. Sam bought 3 packs of pencils. Each pack has 8 pencils. He gave away 5. How many pencils does he have now?</p>
        <input type="radio" name="q5" value="19"> 19<br />
        <input type="radio" name="q5" value="21"> 21<br />
        <input type="radio" name="q5" value="24"> 24
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
        q1: "503",
        q2: "425",
        q3: "72",
        q4: "12",
        q5: "19"
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

      let score = 5;
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
  <title>Grade 6 Quiz – Mealting Maths</title>
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
    <h2 class="text-3xl text-center text-orange-500 mb-6">Grade 6 Arithmetic Quiz</h2>

    <form id="quizForm" class="space-y-6">
      <div>
        <p class="font-semibold">1. What is 1,234 + 789?</p>
        <input type="radio" name="q1" value="2003"> 2003<br />
        <input type="radio" name="q1" value="2023"> 2023<br />
        <input type="radio" name="q1" value="2024"> 2024
      </div>

      <div>
        <p class="font-semibold">2. What is 3,000 − 1,458?</p>
        <input type="radio" name="q2" value="1542"> 1542<br />
        <input type="radio" name="q2" value="1452"> 1452<br />
        <input type="radio" name="q2" value="1442"> 1442
      </div>

      <div>
        <p class="font-semibold">3. What is 45 × 6?</p>
        <input type="radio" name="q3" value="260"> 260<br />
        <input type="radio" name="q3" value="270"> 270<br />
        <input type="radio" name="q3" value="280"> 280
      </div>

      <div>
        <p class="font-semibold">4. What is 225 ÷ 5?</p>
        <input type="radio" name="q4" value="45"> 45<br />
        <input type="radio" name="q4" value="55"> 55<br />
        <input type="radio" name="q4" value="65"> 65
      </div>

      <div>
        <p class="font-semibold">5. A box has 6 rows with 8 pencils in each. If 12 pencils are removed, how many are left?</p>
        <input type="radio" name="q5" value="48"> 48<br />
        <input type="radio" name="q5" value="36"> 36<br />
        <input type="radio" name="q5" value="42"> 42
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
        q1: "2023",
        q2: "1542",
        q3: "270",
        q4: "45",
        q5: "36"
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
