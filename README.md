
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
  <title>Grade 6 Tough Quiz – Mealting Maths</title>
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
    <h2 class="text-3xl text-center text-orange-500 mb-6">Grade 6 Arithmetic Quiz – Tough</h2>

    <form id="quizForm" class="space-y-6">
      <div>
        <p class="font-semibold">1. What is the least common multiple (LCM) of 8, 12, and 18?</p>
        <input type="radio" name="q1" value="72"> 72<br />
        <input type="radio" name="q1" value="36"> 36<br />
        <input type="radio" name="q1" value="144"> 144
      </div>

      <div>
        <p class="font-semibold">2. What is (144 ÷ 6) × (5 + 7) − 24?</p>
        <input type="radio" name="q2" value="240"> 240<br />
        <input type="radio" name="q2" value="264"> 264<br />
        <input type="radio" name="q2" value="252"> 252
      </div>

      <div>
        <p class="font-semibold">3. A train travels 96 km in 3 hours. At the same speed, how far will it travel in 5.5 hours?</p>
        <input type="radio" name="q3" value="160"> 160 km<br />
        <input type="radio" name="q3" value="176"> 176 km<br />
        <input type="radio" name="q3" value="180"> 180 km
      </div>

      <div>
        <p class="font-semibold">4. Which of the following numbers is divisible by both 3 and 4?</p>
        <input type="radio" name="q4" value="126"> 126<br />
        <input type="radio" name="q4" value="132"> 132<br />
        <input type="radio" name="q4" value="138"> 138
      </div>

      <div>
        <p class="font-semibold">5. A basket has 48 mangoes. If 25% get spoiled and the rest are equally packed into 5 boxes, how many mangoes are in each box?</p>
        <input type="radio" name="q5" value="6"> 6<br />
        <input type="radio" name="q5" value="7"> 7<br />
        <input type="radio" name="q5" value="8"> 8
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
        q1: "72",
        q2: "252",
        q3: "176",
        q4: "132",
        q5: "8"
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
  <title>Grade 7 Quiz – Mealting Maths</title>
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
    <h2 class="text-3xl text-center text-orange-500 mb-6">Grade 7 Arithmetic Quiz – Challenging</h2>

    <form id="quizForm" class="space-y-6">
      <div>
        <p class="font-semibold">1. What is the value of (84 ÷ 6) + (13 × 4) − 5?</p>
        <input type="radio" name="q1" value="55"> 55<br />
        <input type="radio" name="q1" value="60"> 60<br />
        <input type="radio" name="q1" value="61"> 61
      </div>

      <div>
        <p class="font-semibold">2. If A = 2 and B = 3, what is the value of (A + B)² − (B − A)²?</p>
        <input type="radio" name="q2" value="28"> 28<br />
        <input type="radio" name="q2" value="20"> 20<br />
        <input type="radio" name="q2" value="16"> 16
      </div>

      <div>
        <p class="font-semibold">3. What is the smallest number divisible by 12, 15, and 18?</p>
        <input type="radio" name="q3" value="180"> 180<br />
        <input type="radio" name="q3" value="90"> 90<br />
        <input type="radio" name="q3" value="60"> 60
      </div>

      <div>
        <p class="font-semibold">4. Find the value of: 144 − 48 ÷ 4 × 3</p>
        <input type="radio" name="q4" value="108"> 108<br />
        <input type="radio" name="q4" value="111"> 111<br />
        <input type="radio" name="q4" value="120"> 120
      </div>

      <div>
        <p class="font-semibold">5. A number is increased by 20% and then decreased by 25%. What is the net change?</p>
        <input type="radio" name="q5" value="5% decrease"> 5% decrease<br />
        <input type="radio" name="q5" value="10% decrease"> 10% decrease<br />
        <input type="radio" name="q5" value="No change"> No change
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
        q1: "60",
        q2: "28",
        q3: "180",
        q4: "111",
        q5: "10% decrease"
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
  <title>Grade 8 Quiz – Mealting Maths</title>
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
    <h2 class="text-3xl text-center text-orange-500 mb-6">Grade 8 Arithmetic Quiz – Tough</h2>

    <form id="quizForm" class="space-y-6">
      <div>
        <p class="font-semibold">1. Evaluate: (−12 + 5) × (−3)</p>
        <input type="radio" name="q1" value="−21"> −21<br />
        <input type="radio" name="q1" value="−27"> −27<br />
        <input type="radio" name="q1" value="−36"> −36
      </div>

      <div>
        <p class="font-semibold">2. If x = 4 and y = −2, what is the value of: x² − y³?</p>
        <input type="radio" name="q2" value="24"> 24<br />
        <input type="radio" name="q2" value="8"> 8<br />
        <input type="radio" name="q2" value="32"> 32
      </div>

      <div>
        <p class="font-semibold">3. What is the reciprocal of −5/6?</p>
        <input type="radio" name="q3" value="−6/5"> −6/5<br />
        <input type="radio" name="q3" value="5/6"> 5/6<br />
        <input type="radio" name="q3" value="−5/6"> −5/6
      </div>

      <div>
        <p class="font-semibold">4. If the original price of a jacket is ₹1200 and it is increased by 15%, what is the new price?</p>
        <input type="radio" name="q4" value="₹1380"> ₹1380<br />
        <input type="radio" name="q4" value="₹1350"> ₹1350<br />
        <input type="radio" name="q4" value="₹1320"> ₹1320
      </div>

      <div>
        <p class="font-semibold">5. Simplify: 3a − 2b + 4a + b</p>
        <input type="radio" name="q5" value="7a − b"> 7a − b<br />
        <input type="radio" name="q5" value="6a + 3b"> 6a + 3b<br />
        <input type="radio" name="q5" value="7a − 3b"> 7a − 3b
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
        q1: "−21",
        q2: "32",
        q3: "−6/5",
        q4: "₹1380",
        q5: "7a − b"
      };

      let score = 0;
      const form = document.forms["quizForm"];
      for (const key in correctAnswers) {
        if (form[key].value === correctAnswers[key]) {
          score++;
        }
      }

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

