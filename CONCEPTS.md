# Concept Glossary

Use this glossary as a living reference. Add examples as the bootcamp grows.

## Program

Definition: A set of instructions a computer can run.

Beginner explanation: A program tells the computer what to do, step by step.

Example:

```python
print("Welcome to Track Career Analyzer")
```

Analogy: A workout plan for a computer.

Why it matters: Every app starts as a program.

Questions: What instructions does this program give the computer?

## Python

Definition: A beginner-friendly programming language.

Beginner explanation: Python lets you write instructions using readable text.

Example:

```bash
python3 app.py
```

Analogy: A language you and the computer can both work with.

Why it matters: This bootcamp uses Python to build the app.

Questions: How do you run a Python file?

## Terminal

Definition: An app for typing commands to the computer.

Beginner explanation: Terminal is a text-based way to move around files and run tools.

Example:

```bash
pwd
ls
cd app
python3 app.py
```

Analogy: A command center.

Why it matters: Developers use Terminal constantly.

Questions: What folder are you in? How can you tell?

## VS Code

Definition: A code editor.

Beginner explanation: VS Code is where you write and organize project files.

Example:

```bash
code .
```

Analogy: A notebook and workshop for code.

Why it matters: This is where most coding happens.

Questions: What is the difference between VS Code and Terminal?

## Directory, File, and Path

Definition: A directory is a folder, a file stores content, and a path tells where something lives.

Beginner explanation: Projects are organized with folders and files.

Example:

```text
app/data/sample_results.csv
```

Analogy: A locker, binder, and page location.

Why it matters: Code often needs to find files by path.

Questions: Where is `sample_results.csv` located?

## Variable

Definition: A named value in a program.

Beginner explanation: A variable stores information so code can use it later.

Example:

```python
athlete_name = "Riley"
```

Analogy: A labeled box.

Why it matters: Programs need to remember data.

Questions: What value is stored in this variable?

## String, Number, and Boolean

Definition: Common data types for text, numeric values, and true/false values.

Beginner explanation: Different kinds of information behave differently in code.

Example:

```python
name = "Riley"
graduation_year = 2026
is_senior = True
```

Analogy: Different event types in track need different rules.

Why it matters: Bugs often happen when data is the wrong type.

Questions: Which values are text? Which are numbers?

## Conditional

Definition: Code that makes a decision.

Beginner explanation: `if`, `elif`, and `else` let the program choose what to do.

Example:

```python
if current_mark >= goal_mark:
    print("Goal reached")
else:
    print("Keep chasing")
```

Analogy: If it rains, practice moves indoors.

Why it matters: Apps need to respond to different situations.

Questions: What condition is being checked?

## List and Loop

Definition: A list stores multiple values. A loop repeats code.

Beginner explanation: Lists and loops help with multiple results.

Example:

```python
results = [12.1, 11.9, 11.8]

for result in results:
    print(result)
```

Analogy: A season schedule and going through each meet.

Why it matters: Real data usually has many items.

Questions: How many times will the loop run?

## Function

Definition: A reusable block of code with a name.

Beginner explanation: Functions help organize programs into smaller pieces.

Example:

```python
def show_welcome():
    print("Welcome")
```

Analogy: A repeatable warmup routine.

Why it matters: Clean code is easier to read, test, and fix.

Questions: What does this function do?

## Parameter and Return Value

Definition: A parameter is input to a function. A return value is output from a function.

Beginner explanation: Functions can receive information and send information back.

Example:

```python
def double(number):
    return number * 2
```

Analogy: Give a coach a time, get a training pace back.

Why it matters: Functions become more useful when they work with different values.

Questions: What goes in? What comes out?

## CSV

Definition: A comma-separated values file.

Beginner explanation: A simple text file for table-like data.

Example:

```csv
date,event,mark,meet
2026-04-12,400m,58.2,Spring Invite
```

Analogy: A spreadsheet saved as plain text.

Why it matters: CSV files are a simple way to save app data.

Questions: What are the columns?

## pandas DataFrame

Definition: A table-like data structure from the pandas library.

Beginner explanation: A DataFrame is like a spreadsheet inside Python.

Example:

```python
import pandas as pd

df = pd.read_csv("data/sample_results.csv")
print(df.head())
```

Analogy: Excel inside your Python program.

Why it matters: DataFrames make analysis easier.

Questions: What does each row represent?

## Streamlit

Definition: A Python library for building simple web apps.

Beginner explanation: Streamlit turns Python code into a browser app.

Example:

```bash
streamlit run streamlit_app.py
```

Analogy: Turning a notebook into a dashboard.

Why it matters: The final app should be easy to demo and view on a phone.

Questions: How is a Streamlit app different from a terminal app?

## Git and GitHub

Definition: Git tracks project history. GitHub stores Git repositories online.

Beginner explanation: Git saves snapshots locally. GitHub keeps a remote copy and supports review.

Example:

```bash
git status
git add .
git commit -m "Add first Python program"
git push
```

Analogy: Git is local save history. GitHub is the shared team copy.

Why it matters: Developers use Git and GitHub to protect work and collaborate.

Questions: What is the difference between commit and push?

## Branch, Pull Request, Merge, and Remote

Definition: A branch is a separate line of work. A pull request asks to review and combine work. Merge combines it. A remote is an online copy.

Beginner explanation: Branches let you work safely before updating `main`.

Example:

```bash
git switch -c phase-01-first-python
```

Analogy: Drafting an essay before putting it in the final folder.

Why it matters: Branches and PRs make practice safer.

Questions: Why not do all work directly on `main`?

## Debugging and Error Message

Definition: Debugging is finding and fixing problems. An error message explains what went wrong.

Beginner explanation: Bugs are normal. Error messages are clues.

Example:

```text
NameError: name 'athlete' is not defined
```

Analogy: A coach spotting what went wrong in a race plan.

Why it matters: Debugging is one of the most important programming skills.

Questions: What line did the error happen on?

## AI Pair Programmer

Definition: AI used as a coding partner.

Beginner explanation: AI can explain, review, and suggest, but the student owns the understanding.

Example:

```text
Please give me one hint about this error, not the full answer.
```

Analogy: A coach who asks questions and gives feedback.

Why it matters: AI is powerful, but learning requires active thinking.

Questions: Can you explain the code AI helped with?

