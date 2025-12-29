<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quiz for Dangerous Korede</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background: #fce4ec;
            color: #333;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 20px;
        }

        h1 {
            color: #e91e63;
        }

        .quiz-container {
            background: #fff;
            padding: 20px 30px;
            border-radius: 15px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
            max-width: 500px;
            width: 100%;
        }

        .question {
            margin-bottom: 15px;
            font-weight: bold;
        }

        .options {
            list-style: none;
            padding: 0;
        }

        .options li {
            margin: 8px 0;
        }

        button {
            background: #e91e63;
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 8px;
            cursor: pointer;
            margin-top: 15px;
        }

        button:hover {
            background: #c2185b;
        }

        .result {
            margin-top: 20px;
            font-weight: bold;
            font-size: 1.2em;
            color: #4caf50;
        }
    </style>
</head>
<body>
    <h1>Something for Dangerous KOREDE 😎</h1>
    <div class="quiz-container">
        <div id="quiz"></div>
        <button onclick="checkAnswers()">Submit Answers</button>
        <div id="result" class="result"></div>
    </div>

    <script>
        const quizData = [
            {
                question: "1. What's Dangerous Korede's secret superpower?",
                options: ["Sweet and Caring", "Making people laugh", "Agbero", "Beating men"],
                answer: "Sweet and Caring"
            },
            {
                question: "2. What is Korede's GO TO DESSERT",
                options: ["ICE-CREAM", "FUFU", "RICE", "BREAD AND OGBONO"],
                answer: "ICE-CREAM"
            },
            {
                question: "3. If Korede was a cartoon character, she would be?",
                options: ["SpongeBob", "Mickey Mouse", "Tom from Tom & Jerry", "Dora the Explorer"],
                answer: "SpongeBob"
            },
            {
                question: "4. Dangerous Korede can't live without?",
                options: ["Food", "WiFi", "Sleep", "Coffee"],
                answer: "Food"
            },
            {
                question: "5. Korede's Favourite Artist is?",
                options: ["Juice world", "Burna Boy", "Seyi-Vibes", "Beyonce"],
                answer: "Seyi-Vibes"
            }
            
        ];

        const quizDiv = document.getElementById('quiz');

        quizData.forEach((q, index) => {
            const questionEl = document.createElement('div');
            questionEl.classList.add('question');
            questionEl.innerText = q.question;

            const optionsEl = document.createElement('ul');
            optionsEl.classList.add('options');

            q.options.forEach(option => {
                const li = document.createElement('li');
                li.innerHTML = `<input type="radio" name="q${index}" value="${option}"> ${option}`;
                optionsEl.appendChild(li);
            });

            quizDiv.appendChild(questionEl);
            quizDiv.appendChild(optionsEl);
        });

        function checkAnswers() {
            let score = 0;
            quizData.forEach((q, index) => {
                const selected = document.querySelector(`input[name="q${index}"]:checked`);
                if (selected && selected.value === q.answer) {
                    score++;
                }
            });
            document.getElementById('result').innerText = `You scored ${score} out of ${quizData.length}! 🎉`;
        }
    </script>
</body>
</html>
<h2> THANK YOU FOR PARTICIPATING IN THIS QUIZ BE PREPARED FOR MORE ENJOY YOURSELF FOR NOW </h2>

