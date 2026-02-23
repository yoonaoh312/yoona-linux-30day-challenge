# Day 24: Bash Quiz Game

## 🗓️ Date
2025-09-17

## ✅ Goal
Create a simple interactive Q&A quiz game in Bash using the select command to allow the user to choose answers.

## 🗂️ Key Commands and Their Purpose
| Command / Syntax                        | Description                                         |
|----------------------------------------|-----------------------------------------------------|
| `#!/bin/bash`                           | Define the script as a Bash script                 |
| `select var in option1 option2 ...; do` | Display a menu and store the chosen option in `var`|
| `case $var in ...)`                      | Handle different choices and execute corresponding commands |
| `echo`                                  | Print messages or questions to the terminal       |
| `read`                                  | Read user input (if needed for open-ended input)  |
| `break`                                 | Exit the select loop after a valid answer         |
| `sleep 1`                               | Pause briefly for better user experience          |


## 🔍 What I Did Today

- Created a Bash script named quiz.sh.
- Defined 3–5 questions with 3–4 answer choices each.
- Used the select command to present the choices interactively.
- Implemented a case statement to check if the selected answer is correct.
- Added a scoring mechanism to count correct answers.
- Added feedback messages like "Correct!" or "Try again!" based on the user’s choice.
- Tested the script to ensure the menu loops correctly and exits at the end.

## 🧠 Notes
- select automatically numbers the options, making it easy for the user to choose.
- Always include a break to exit the select loop once the question is answered.
- Use clear and simple prompts to make the game user-friendly.
- Can expand later: shuffle questions, add more questions, or use colors for feedback.
- Keep the script executable: chmod +x quiz.sh before running with ./quiz.sh.