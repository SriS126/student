---
toc: True
comments: True
layout: post
title: IPYNB Table, Code (With Quiz)
description: This shows the basic commands of languages with pseudo code.
courses: {'compsci': {'week': 1}}
type: hacks
---

## Learning College Board Pseudo Code
> College Board uses a kind-of programming language in its Multiple Choice exam. There are thousands of different programming languages have been created, and more are being created every year.  College Board has designed a pseudo code, a non operational programming language, to highlight concepts that it wants every student to learn.

College Board is trying to remain neutral and build Computer Science Principles off of any language, thus the Teacher is left to pick the language(s) according to application and curriculum. 

College Board Pseudo Code [Exam Reference Sheet](https://apcentral.collegeboard.org/media/pdf/ap-computer-science-principles-exam-reference-sheet.pdf)


### Comparison of CB Pseudo Code to Python with descriptions

Command Vocabulary | Pseudo code         | Python                 | Purpose
Output       | DISPLAY(expression) | print(expression, end=" ") | Displays the value of expression, followed by a space. Python defaults to newline, thus the end=" "
Input        | a ← INPUT()         | a = input(prompt)      | Accepts a value from the user and returns it to the variable a.
Assignment   |	a ← expression	   | a = expression         | Evaluates expression and assigns the result to the variable a.
Selection    | IF (expression)     | if expression:         | Run commands in the code block associated with the selection
Iteration n times     |	REPEAT n TIMES      | for i in range(n): | Repeat commands in the code block associated withe the iteration n times
Iteration expression  | REPEAT UNTIL (expression) |	while expression: |  Repeat commands in the code block associated withe the iteration while expression is true
List Assignment | list ← [expression1, expression2, expression3] | list = [expression1, expression2, expression3] | Assigns 3 values to list, value can be literal or expressions
First index in List     |	list[1] | list[0] | Access the 1st element in the list[].  FYI, most programming languages start a zero.
Last index in List    | list[LENGTH(list)] | list[len(list) - 1] | Access the last element in the list[].  If you start at zero, last element is length - 1.
Define Procedure      | PROCEDURE name (parameter) | def name(parameter): |  Create a procedure containing a sequence of programming instructions.
Expression equals     |	a = b	| a == b  | Evaluate if assigned value of a equals assigned value of b
Expression not equals |	a ≠ b	| a != b  | Evaluate if assigned value of a is NOT equal to assigned value of b

### Pseudo code IF Code Block
```
a ← 1
b ← 1

IF (a = b) {
   DISPLAY("A equals B")
}
```


```python
# Python code if block to match Pseudo Code
a = 1
b = 1
if (a == b):
    # Python uses indent to establish code block, Teacher use tab key
    print("A equals B")
```

    A equals B


## Hacks
> Key Learnings.  It is very important that you become fluent in " Vocabulary" and researching problems.

- Code a JavaScript cell, this must start with %%js%% in first line of cell. Match the IF condition example in this blog.

- Code a REPEAT n TIMES as described in comparison sheet in Pseudo code, Python, and JavaScript.  Be sure to comment your code.
    -  REPEAT 100 TIMES
    -  Sum all the numpers
    -  PRINT the result

- Reflect on our PSEUDO code and how it helped with your problem solving in these hacks.  

- Maked efinition for: code block, sequence, selections, iteration.  Consider a strategy to remember Pseudo Code, Python and JavaScript for these definitions.

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Programming Concepts Quiz</title>
</head>
<body>
    <h1>Programming Concepts Quiz</h1>
    <form id="quizForm">
        <ol>
            <li>
                <h3>What does the following code do in Python?</h3>
                <code>DISPLAY(expression)</code>
                <label>
                    <input type="radio" name="q1" value="correct">Displays the value of expression, followed by a space.
                </label>
                <label>
                    <input type="radio" name="q1" value="incorrect">Accepts a value from the user and assigns it to a variable.
                </label>
            </li>
            <li>
                <h3>What is the purpose of the following code in Python?</h3>
                <code>a ← INPUT()</code>
                <label>
                    <input type="radio" name="q2" value="incorrect">Displays the value of a variable.
                </label>
                <label>
                    <input type="radio" name="q2" value="correct">Accepts a value from the user and assigns it to a variable.
                </label>
            </li>
            <li>
                <h3>What does the following code represent in Python?</h3>
                <code>a ← expression</code>
                <label>
                    <input type="radio" name="q3" value="correct">Evaluates expression and assigns the result to the variable a.
                </label>
                <label>
                    <input type="radio" name="q3" value="incorrect">Displays the value of expression.
                </label>
            </li>
            <li>
                <h3>What is the purpose of the following code in Python?</h3>
                <code>IF (expression)</code>
                <label>
                    <input type="radio" name="q4" value="correct">Runs commands in the code block associated with the selection if the expression is true.
                </label>
                <label>
                    <input type="radio" name="q4" value="incorrect">Accepts user input.
                </label>
            </li>
            <li>
                <h3>How can you repeat a block of code in Python 'n' times?</h3>
                <code>REPEAT n TIMES</code>
                <label>
                    <input type="radio" name="q5" value="correct">Using a for loop with a range of 'n'.
                </label>
                <label>
                    <input type="radio" name="q5" value="incorrect">Using a while loop with a condition 'n'.
                </label>
            </li>
            <li>
                <h3>How do you access the first element in a list in Python?</h3>
                <code>list[1]</code>
                <label>
                    <input type="radio" name="q6" value="incorrect">Access the first element.
                </label>
                <label>
                    <input type="radio" name="q6" value="correct">Access the second element.
                </label>
            </li>
            <li>
                <h3>What is the purpose of the following code in Python?</h3>
                <code>REPEAT UNTIL (expression)</code>
                <label>
                    <input type="radio" name="q7" value="correct">Repeat commands in the code block associated with the iteration while the expression is true.
                </label>
                <label>
                    <input type="radio" name="q7" value="incorrect">Repeat a fixed number of times.
                </label>
            </li>
            <li>
                <h3>How can you access the last element in a Python list?</h3>
                <code>list[LENGTH(list)]</code>
                <label>
                    <input type="radio" name="q8" value="incorrect">Access the first element.
                </label>
                <label>
                    <input type="radio" name="q8" value="correct">Access the last element.
                </label>
            </li>
            <!-- Add 2 more questions here -->
            <li>
                <h3>What is the purpose of the following code in Python?</h3>
                <code>PROCEDURE name (parameter)</code>
                <label>
                    <input type="radio" name="q9" value="correct">Create a procedure containing a sequence of programming instructions.
                </label>
                <label>
                    <input type="radio" name="q9" value="incorrect">Assign a value to a variable.
                </label>
            </li>
            <li>
                <h3>How is the equality of two values checked in Python?</h3>
                <code>a = b</code>
                <label>
                    <input type="radio" name="q10" value="incorrect">Using a single equal sign (=).
                </label>
                <label>
                    <input type="radio" name="q10" value="correct">Using a double equal sign (==).
                </label>
            </li>
        </ol>
        <input type="submit" value="Submit Quiz">
    </form>

    <script>
        const quizForm = document.getElementById("quizForm");
        quizForm.addEventListener("submit", function (e) {
            e.preventDefault();

            const answers = {
                q1: "correct",
                q2: "correct",
                q3: "correct",
                q4: "correct",
                q5: "correct",
                q6: "incorrect",
                q7: "correct",
                q8: "correct",
                q9: "correct",
                q10: "correct",
                // Add answers for the remaining questions
            };

            let score = 0;
            for (const question in answers) {
                const selectedAnswer = document.querySelector(`input[name=${question}]:checked`);
                if (selectedAnswer) {
                    if (selectedAnswer.value === answers[question]) {
                        score++;
                    }
                }
            }

            alert(`You scored ${score} out of 10.`);
        });
    </script>
</body>