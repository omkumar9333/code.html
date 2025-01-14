<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Online Exam Form</title>
  <link rel="stylesheet" href="styles.css">
</head>

<body>
  <div class="container">
    <h1>Online Exam Form</h1>
    <form>
      <input type="text" placeholder="email id">
      <input type="text" placeholder="password">

    </form>
    <br>
    <label for="id3">
      <input type="radio" value="class IInd year" name="class" id="id3">class IInd year
    </label>
    <br>


    <select name="Division" id="Division">
      <option value="A">A</option>
      <option value="B">B</option>
    </select>


    <br>
    <form>
      <input type="Digit" placeholder="Roll No">
    </form>
    <br>
    <form id="examForm">
      <div class="question">
        <p>1. What is Project-Based Learning (PBL)?</p>
        <label>
          <input type="radio" name="q1" value="actively engaging in real-world."> actively engaging in real-world.
        </label>
        <br>
        <label>
          <input type="radio" name="q1" value="instructional methodology."> instructional methodology.
        </label>
        <br>
        <label>
          <input type="radio" name="q1" value="meaningful projects."> meaningful projects.
        </label>
        <br>
        <label>
          <input type="radio" name="q1" value="All of the above.">All of the above.
        </label>
        <br>

      </div>
      <br>
      <div class="question">
        <p>2. How does PBL differ from traditional learning methods?</p>
        <label>
          <input type="radio" name="q2"
            value="In traditional learning, students often receive information passively through lectures or textbooksPBL, on the other hand, involves students in active, real-world problem-solving where they work on projects ">
          In traditional learning, students often receive information passively through lectures or textbooks PBL, on
          the other hand, involves students in active, real-world problem-solving where they work on projects
        </label>
        <br>
        <label>
          <input type="radio" name="q2"
            value="You can expand upon this with more questions, features like a timer, and form validation for a more robust application.">
          You can expand upon this with more questions, features like a timer, and form validation for a more robust
          application.
        </label>
        <br>
        <label>
          <input type="radio" name="q2"
            value="the teacher is the primary source of knowledge and authority in the classroom. The teacher delivers content to the students through lectures or direct instruction.">
          the teacher is the primary source of knowledge and authority in the classroom. The teacher delivers content to
          the students through lectures or direct instruction.
        </label>
        <br>
        <label>
          <input type="radio" name="q2"
            value="Students are typically passive recipients of information. They listen to lectures, take notes, and absorb the content delivered by the teacher.">Students
          are typically passive recipients of information. They listen to lectures, take notes, and absorb the content
          delivered by the teacher.
        </label>
        <br>
      </div>
      <div class="question">
        <p>3. What are the benefits of Project-Based Learning?</p>
        <label>
          <input type="radio" name="q3" value="Critical thinking and problem-solving skills"> Critical thinking and
          problem-solving skills
        </label>
        <br>
        <label>
          <input type="radio" name="q3" value="Long-term retention"> Long-term retention
        </label>
        <br>
        <label>
          <input type="radio" name="q3" value="Preparation for the future"> Preparation for the future
        </label>
        <br>
        </label>
        <input type="radio" name="q3" value="All of the above.">All of the above.
        </label>
        <br>
        <p>4. How do teachers assess students in PBL?</p>
        <label>
          <input type="radio" name="q4" value="Formative and Summative assessments"> Formative and Summative assessments
        </label>
        <br>
        <label>
          <input type="radio" name="q4" value="Long-term retention"> Long-term retention
        </label>
        <br>
        <label>
          <input type="radio" name="q4" value="Preparation for the future"> Preparation for the future
        </label>
        <br>
        </label>
        <input type="radio" name="q4" value="Time constraints.">Time constraints
        </label>
        <br>
        <p>5. How do students benefit from collaboration in PBL?</p>
        <form>
          <input type="text" placeholder="Answer">
        </form>
        <br>
      </div>
      <button type="button" onclick="checkResults()">Submit</button>
    </form>
    <div id="result" class="result"></div>
  </div>

  <script src="script.js"></script>
</body>

</html>
body {
font-family: Arial, sans-serif;
background-color: #f4f4f4;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}

.container {
background-color: white;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
width: 300px;
}

h1 {
text-align: center;
}

.question {
margin-bottom: 15px;
}

label {
display: block;
margin: 5px 0;
}

button {
width: 100%;
padding: 10px;
background-color: #4CAF50;
color: white;
border: none;
cursor: pointer;
border-radius: 5px;
}

button:hover {
background-color: #45a049;
}

.result {
margin-top: 20px;
text-align: center;
}
function checkResults() {
let score = 0;

// Get the form elements
const form = document.getElementById('examForm');

// Check answers for each question
if (form.q1.value === 'All of the above') {
score++;
}
if (form.q2.value === ' In traditional learning, students often receive information passively through lectures or
textbooks PBL, on the other hand, involves students in active, real-world problem-solving where they work on projects'){
score++;
}
if (form.q3.value === 'All of the above') {
score++;
}
if (form.q4.value === 'Formative and Summative assessments') {
score++;
}
if (form.q5.value === 'Collaboration in PBL helps students develop important interpersonal skills such as communication,
conflict resolution, and teamwork. Working in teams allows them to leverage diverse perspectives and skills, and helps
them learn how to divide tasks, share responsibilities, and collaborate effectively to achieve common goals.') {
score++;
}

// Display the result
const resultDiv = document.getElementById('result');
resultDiv.innerHTML = Your score is: ${score} out of 10;

// Prevent form submission
return false;

// You can add more logic here for different results (e.g., feedback based on score)
if (score === 10) {
resultDiv.innerHTML += "<br>Excellent!";
} else if (score === 8) {
resultDiv.innerHTML += "<br>Good job!";
} else if (score === 6) {
resultDiv.innerHTML += "<br>Nice!";
else if (score === 4){
resultDiv.innerHTML += "<br>Okay!";
} else if (score === 2){
resultDiv.innerHTML += "<br>Keep trying!";
} else {
resultDiv.innerHTML += "<br>Better luck next time!";
}
}
