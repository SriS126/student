---
toc: true
comments: false
layout: post
title: Superhero Quiz!!!
description: A basic quiz about some superheros, can you get them all right?
type: hacks
courses: { compsci: {week: 2} }
---

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Superhero Quiz</title>
</head>
<body>
    <h1>Superhero Quiz</h1>
    <form id="quiz-form">
        <p>1. Who is known as the "Man of Steel"?</p>
        <label>
            <input type="radio" name="q1" value="a">a) Spider-Man
        </label><br>
        <label>
            <input type="radio" name="q1" value="b">b) Batman
        </label><br>
        <label>
            <input type="radio" name="q1" value="c">c) Superman
        </label><br>

        <p>2. Which superhero is billionaire playboy Tony Stark?</p>
        <label>
            <input type="radio" name="q2" value="a">a) The Flash
        </label><br>
        <label>
            <input type="radio" name="q2" value="b">b) Iron Man
        </label><br>
        <label>
            <input type="radio" name="q2" value="c">c) Green Lantern
        </label><br>

        <p>3. Who is the alter ego of Diana Prince?</p>
        <label>
            <input type="radio" name="q3" value="a">a) Wonder Woman
        </label><br>
        <label>
            <input type="radio" name="q3" value="b">b) Catwoman
        </label><br>
        <label>
            <input type="radio" name="q3" value="c">c) Black Widow
        </label><br>

        <p>4. Which superhero has the power of the "Speed Force"?</p>
        <label>
            <input type="radio" name="q4" value="a">a) The Hulk
        </label><br>
        <label>
            <input type="radio" name="q4" value="b">b) The Flash
        </label><br>
        <label>
            <input type="radio" name="q4" value="c">c) Thor
        </label><br>

        <p>5. What is the real name of the superhero who is known for his detective skills and the Bat-Signal?</p>
        <label>
            <input type="radio" name="q5" value="a">a) Bruce Banner
        </label><br>
        <label>
            <input type="radio" name="q5" value="b">b) Bruce Wayne
        </label><br>
        <label>
            <input type="radio" name="q5" value="c">c) Clark Kent
        </label><br>

        <p>6. Who is the Norse god of thunder in the Marvel Universe?</p>
        <label>
            <input type="radio" name="q6" value="a">a) Loki
        </label><br>
        <label>
            <input type="radio" name="q6" value="b">b) Thor
        </label><br>
        <label>
            <input type="radio" name="q6" value="c">c) Captain America
        </label><br>

        <br>
        <input type="submit" value="Submit">
    </form>

    <script>
        document.getElementById("quiz-form").addEventListener("submit", function(event) {
            event.preventDefault();
            let score = 0;
            const answers = ["c", "b", "a", "b", "b", "b"];
            
            for (let i = 1; i <= 6; i++) {
                const selectedOption = document.querySelector(`input[name="q${i}"]:checked`);
                if (selectedOption) {
                    if (selectedOption.value === answers[i - 1]) {
                        score++;
                    }
                }
            }
            
            alert(`You scored ${score} out of 6.`);
        });
    </script>
</body>