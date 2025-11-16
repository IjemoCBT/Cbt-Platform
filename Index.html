<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CBT Platform</title>
<style>
    body { font-family: Arial, sans-serif; background: #f4f4f4; margin: 0; padding: 0; }
    .container { width: 90%; max-width: 500px; margin: 50px auto; background: #fff; padding: 20px;
        border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
    h2 { text-align: center; }
    button { width: 100%; padding: 12px; margin-top: 10px; font-size: 16px; cursor: pointer; }
    input, select { width: 100%; padding: 10px; margin-top: 10px; font-size: 14px; }
    .hidden { display: none; }
    .question-box { margin-bottom: 20px; }
    .result-box { padding: 10px; background: #eaeaea; margin-top: 20px; }
</style>
</head>
<body>

<div id="loginPage" class="container">
    <h2>CBT Login</h2>
    <input id="username" placeholder="Enter Username">
    <input id="password" placeholder="Enter Password" type="password">
    <button onclick="login()">Login</button>
</div>

<div id="adminPage" class="container hidden">
    <h2>Admin Dashboard</h2>

    <h3>Add Student</h3>
    <input id="stuName" placeholder="Student Name">
    <input id="stuPass" placeholder="Password">
    <button onclick="addStudent()">Add Student</button>

    <h3>Add Question</h3>
    <select id="subject">
        <option value="Mathematics">Mathematics</option>
        <option value="Physics">Physics</option>
        <option value="Biology">Biology</option>
        <option value="Chemistry">Chemistry</option>
        <option value="English">English</option>
    </select>

    <input id="qText" placeholder="Question">
    <input id="optA" placeholder="Option A">
    <input id="optB" placeholder="Option B">
    <input id="optC" placeholder="Option C">
    <input id="optD" placeholder="Option D">
    <input id="correct" placeholder="Correct Option (A/B/C/D)">
    <button onclick="addQuestion()">Add Question</button>
</div>

<div id="studentPage" class="container hidden">
    <h2>Choose Subject</h2>
    <select id="subSelect"></select>
    <button onclick="startExam()">Start Exam</button>
</div>

<div id="examPage" class="container hidden">
    <h2 id="examSubject"></h2>
    <h3 id="timer">Time: 5:00</h3>
    <div id="questionsArea"></div>
    <button onclick="submitExam()">Submit</button>
</div>

<div id="resultPage" class="container hidden">
    <h2>Your Result</h2>
    <div id="resultDetails"></div>
    <button onclick="goHome()">Finish</button>
</div>

<script>
let students = JSON.parse(localStorage.getItem("students") || "{}");
let questions = JSON.parse(localStorage.getItem("questions") || "{}");
let currentUser = "";
let examTimer;

function login() {
    let user = username.value.trim();
    let pass = password.value.trim();

    if (user === "admin" && pass === "1234") {
        show(adminPage);
        return;
    }

    if (students[user] && students[user] === pass) {
        currentUser = user;
        loadSubjects();
        show(studentPage);
    } else {
        alert("Invalid login");
    }
}

function addStudent() {
    students[stuName.value] = stuPass.value;
    localStorage.setItem("students", JSON.stringify(students));
    alert("Student Added");
}

function addQuestion() {
    let sub = subject.value;
    if (!questions[sub]) questions[sub] = [];

    questions[sub].push({
        q: qText.value,
        A: optA.value,
        B: optB.value,
        C: optC.value,
        D: optD.value,
        correct: correct.value.toUpperCase()
    });

    localStorage.setItem("questions", JSON.stringify(questions));
    alert("Question Added!");
}

function loadSubjects() {
    subSelect.innerHTML = "";
    for (let s in questions) {
        let opt = document.createElement("option");
        opt.value = s;
        opt.innerText = s;
        subSelect.appendChild(opt);
    }
}

function startExam() {
    let sub = subSelect.value;
    examSubject.innerText = sub;

    let qList = questions[sub];
    questionsArea.innerHTML = "";

    qList.forEach((q, i) => {
        questionsArea.innerHTML += `
            <div class='question-box'>
                <b>${i+1}. ${q.q}</b><br>
                <input type='radio' name='q${i}' value='A'> A. ${q.A}<br>
                <input type='radio' name='q${i}' value='B'> B. ${q.B}<br>
                <input type='radio' name='q${i}' value='C'> C. ${q.C}<br>
                <input type='radio' name='q${i}' value='D'> D. ${q.D}<br>
            </div>
        `;
    });

    show(examPage);
    startTimer(300);
}

function startTimer(time) {
    examTimer = setInterval(() => {
        let min = Math.floor(time / 60);
        let sec = time % 60;

        timer.innerText = `Time: ${min}:${sec < 10 ? '0'+sec : sec}`;

        if (time <= 0) {
            clearInterval(examTimer);
            submitExam();
        }

        time--;
    }, 1000);
}

function submitExam() {
    clearInterval(examTimer);

    let sub = examSubject.innerText;
    let qList = questions[sub];
    let correct = 0;

    qList.forEach((q, i) => {
        let ans = document.querySelector(`input[name="q${i}"]:checked`);
        if (ans && ans.value === q.correct) correct++;
    });

    let score = `${correct} / ${qList.length}`;

    resultDetails.innerHTML = `
        <h3>Subject: ${sub}</h3>
        <p>Score: <b>${score}</b></p>
    `;

    show(resultPage);
}

function goHome() {
    show(loginPage);
}

function show(page) {
    loginPage.classList.add("hidden");
    adminPage.classList.add("hidden");
    studentPage.classList.add("hidden");
    examPage.classList.add("hidden");
    resultPage.classList.add("hidden");
    page.classList.remove("hidden");
}
</script>

</body>
</html>
