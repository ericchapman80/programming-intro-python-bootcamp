# Phase 02: Variables, Input, and Athlete Profile

## Goal

Use variables and `input()` to create a simple athlete profile.

By the end of this phase, you should be able to ask the user questions, store answers in variables, convert text input into numbers when needed, and print a formatted athlete profile.

> [!TIP]
> Phase 02 is where the app stops talking at the user and starts listening.

## At A Glance

| You will | What it teaches |
| --- | --- |
| Store a name in a variable | Programs remember values |
| Use `input()` | Programs can ask questions |
| Convert text to numbers | Data types matter |
| Print a profile | Variables can drive output |
| Explain one conversion error | Debugging starts with reading |

## Why This Phase Matters

Most useful programs need information from the user.

In Phase 01, the app printed the same messages every time. In Phase 02, the app starts responding to the person running it.

This is the first step toward making Track Career Analyzer feel like an actual app.

## Time Estimate

Plan for 90-120 minutes.

This phase introduces several core ideas. Move slowly and test after each small change.

## Before You Start

You should be able to:

- Run `python3 app.py`.
- Explain what `print()` does.
- Make a small edit to `app/app.py`.
- Use a branch and pull request.

## New Concepts

### Variable

A variable is a name that stores a value.

Example:

```python
athlete_name = "Riley"
```

Think of a variable like a labeled box. The label is `athlete_name`, and the value inside is `"Riley"`.

### `input()`

`input()` asks the user a question and waits for an answer.

Example:

```python
athlete_name = input("Athlete name: ")
```

Whatever the user types is stored in `athlete_name`.

### String

A string is text.

Example:

```python
primary_event = "400m"
```

Strings usually go inside quotation marks.

### Number

A number can be used for math or comparisons.

Example:

```python
graduation_year = 2026
```

### Type Conversion

`input()` always gives Python text, even if the user types a number.

> [!IMPORTANT]
> This is a classic beginner moment: `input()` returns text. Use `int()` or `float()` only when the program needs a number.

If you want a whole number, use `int()`:

```python
graduation_year = int(input("Graduation year: "))
```

If you want a decimal number, use `float()`:

```python
current_pr = float(input("Current PR: "))
```

Do not worry if this feels strange at first. This is one of the most common beginner Python concepts.

### f-string

An f-string lets you put variable values inside printed text.

Example:

```python
print(f"{athlete_name} runs the {primary_event}.")
```

## Step 1: Start From `main`

Make sure your local `main` branch is up to date:

```bash
git switch main
git pull
```

Create your Phase 02 branch:

```bash
git switch -c phase-02-athlete-profile
```

If the branch already exists, use:

```bash
git switch phase-02-athlete-profile
```

Check:

```bash
git status
```

Expected idea: Git should say you are on branch `phase-02-athlete-profile`.

## Step 2: Run The Current App

Run the app before changing it:

```bash
cd app
python3 app.py
cd ..
```

Notice that the app prints fixed messages. It does not ask the user anything yet.

## Step 3: Add One Variable

Open:

```text
app/app.py
```

Add a variable near the top:

```python
athlete_name = "Riley"
```

Then print it:

```python
print(athlete_name)
```

Run the app:

```bash
cd app
python3 app.py
cd ..
```

Before moving on, explain out loud:

- What is the variable name?
- What value is stored in it?
- Where does it get printed?

## Step 4: Replace The Fixed Variable With `input()`

Change:

```python
athlete_name = "Riley"
```

To:

```python
athlete_name = input("Athlete name: ")
```

Run the app again.

When Terminal asks for a name, type one and press Return.

The app should print the name you entered.

## Step 5: Ask For Profile Details

Add more inputs:

```python
athlete_name = input("Athlete name: ")
graduation_year = int(input("Graduation year: "))
primary_event = input("Primary event: ")
current_pr = float(input("Current PR: "))
```

Use simple values while testing:

```text
Athlete name: Riley
Graduation year: 2026
Primary event: 400m
Current PR: 57.85
```

For this phase, use decimal numbers for marks so Python can practice `float()`.

Later phases can handle more realistic track formats like minutes, seconds, feet, or inches.

## Step 6: Print A Formatted Profile

Use f-strings to print a clean profile:

```python
print()
print("Athlete Profile")
print("---------------")
print(f"Name: {athlete_name}")
print(f"Graduation year: {graduation_year}")
print(f"Primary event: {primary_event}")
print(f"Current PR: {current_pr}")
```

Run the app and confirm the profile uses the values you typed.

## Step 7: Improve The Labels

Make the output easy to read.

For example:

```python
print(f"Current PR: {current_pr} seconds")
```

This is not perfect for every track event, but it is good enough for Phase 02.

Do not build complex event-specific formatting yet.

## Step 8: Practice A Type Conversion Error

This step is optional but useful.

> [!WARNING]
> Practice the error, then return to valid numeric input. The final PR should run cleanly.

Run the app and type words when it asks for graduation year:

```text
Graduation year: senior
```

Python should show an error.

Read the error message. Look for:

- The line number
- `ValueError`
- The value Python could not convert

Run the app again with a number:

```text
Graduation year: 2026
```

Do not commit broken code.

## Step 9: Create Your Phase Reflection

Create:

```text
reflections/phase-02-reflection.md
```

Use the template from:

```text
reflections/phase-reflection-template.md
```

Fill in short answers for:

- What variables are
- What `input()` does
- Why `input()` returns text
- What `int()` or `float()` does
- One error or mistake you saw
- Whether you used AI

## Step 10: Check Your Work With Git

From the main repository folder, run:

```bash
git status
```

You should normally see:

```text
app/app.py
reflections/phase-02-reflection.md
```

Review the code change:

```bash
git diff app/app.py
```

## Step 11: Commit And Push

Stage only the Phase 02 files:

```bash
git add app/app.py reflections/phase-02-reflection.md
```

Commit:

```bash
git commit -m "Complete phase 02 athlete profile"
```

Push:

```bash
git push -u origin phase-02-athlete-profile
```

## Step 12: Open A Pull Request

Open a pull request from:

```text
phase-02-athlete-profile -> main
```

Fill out the pull request template.

In the AI disclosure, include any prompt you used to understand variables, `input()`, or an error message.

## Common Stuck Points

### The program looks frozen after `input()`

It is probably waiting for you to type an answer.

Type a response and press Return.

### `ValueError` when using `int()` or `float()`

Python could not convert the typed text into a number.

Examples that fail:

```text
senior
57 seconds
fifty seven
```

Examples that work:

```text
2026
57.85
```

### The profile prints the wrong value

Check that the variable names match.

Example:

```python
primary_event = input("Primary event: ")
print(f"Primary event: {primary_event}")
```

### `NameError`

Python is trying to use a variable that does not exist yet or is spelled differently.

Check capitalization and spelling.

These are different variable names:

```python
athlete_name
athleteName
Athlete_name
```

## AI Guidelines For This Phase

Good AI prompts:

```text
I am in Phase 02. Explain why input() returns text, using a beginner example.
```

```text
I got this ValueError when using int(). Explain the error, but do not rewrite my whole program.
```

```text
Ask me questions to check whether I understand variables and type conversion.
```

Avoid prompts like:

```text
Write the complete Phase 02 athlete profile program for me.
```

## Demo

Show:

- `app/app.py` in VS Code.
- The app running in Terminal.
- Two different athlete profiles entered through `input()`.
- Your Phase 02 reflection.

Explain:

- What a variable is.
- What `input()` does.
- Why `input()` returns text.
- Why `int()` or `float()` might be needed.
- What an f-string does.
- One error or mistake you saw.
- How AI helped, if you used it.

Live change:

- Add one new profile field, such as hometown, team, or favorite event.
- Save the file.
- Run the app again.
- Explain what code changed.

## Good Enough To Move On

You are ready for Phase 03 when:

- You can run the athlete profile program.
- You can explain every variable in `app/app.py`.
- You can explain why `input()` returns text.
- You can explain one type conversion.
- You can make one small profile-field change without AI.
- You committed and pushed your Phase 02 work.
- You opened a pull request and completed the AI disclosure.
