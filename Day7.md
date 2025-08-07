# Day 7: Bash Scripting Basics – Variables, if/else, Loops

## 🗓️ Date
2025-08-06

## ✅ Goal
Understand the fundamentals of Bash scripting by learning how to use variables, write conditional statements (if/else), and create loops (for, while). Practice writing simple scripts to automate tasks.

## 🗂️ Key Commands and Their Purpose
Command / Syntax	                 Description
variable=value	                     Assign a value to a variable in Bash (no spaces around =).
$variable	                         Access the value stored in a variable.
if condition; then ... else ... fi	 Conditional statement to execute code based on conditions.
for var in list; do ... done	     Loop over a list of values and execute commands for each.
while condition ; do ... done	     Execute commands repeatedly while a condition is true.
read variable	                     Take user input and store it in a variable.

## 🔍 What I Did Today
- Learned to declare and use variables:
name="Yoona"
Used echo to print variable values like echo "Hello, $name"
Practiced if/else statements for decision-making:
Checked number properties (e.g., even/odd)
Used comparison operators such as -eq, -ne, -lt, -le, -gt, -ge
- Explored for and while loops:
Used for i in {1..5}; do echo $i; done to print numbers 1 to 5
Used while loops to repeat actions until a condition changed
Wrote a simple script to ask for user input and print a response based on the input value.

## 🧠 Notes
- Variable assignments do not allow spaces around =.
- Always quote variables inside strings to avoid issues: echo "$name"
- Use double parentheses (( )) for arithmetic evaluation, e.g., if (( num % 2 == 0 )).
- Square brackets [ ] are used for tests and comparisons in conditionals.
- Loops are powerful for automating repetitive tasks and processing lists or files.
- Scripts can be run by making them executable (chmod +x script.sh) and running ./script.sh.

