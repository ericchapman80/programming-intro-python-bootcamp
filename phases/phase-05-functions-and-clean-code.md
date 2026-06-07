# Phase 05: Functions and Cleaner Code

## Goal

Use functions to organize the Track Career Analyzer code into smaller reusable pieces.

By the end of this phase, you should be able to define a function, call a function, pass information into a function with parameters, get information back with a return value, and explain why smaller pieces of code are easier to read.

## Why This Phase Matters

The app has grown across the first few phases.

It now has profile input, goal logic, and multiple results. If everything stays in one long file, the code becomes harder to read, test, and explain.

Functions help you organize code by job.

## Time Estimate

Plan for 90-120 minutes.

This phase is mostly refactoring. Refactoring means changing the structure of code without changing what the program does.

## Before You Start

You should be able to:

- Run `python3 app.py`.
- Explain variables and `input()`.
- Explain `if`, `elif`, and `else`.
- Explain lists and loops.
- Use `append()`, `len()`, and `min()`.
- Commit, push, and open a pull request.

## New Concepts

### Function

A function is a named block of code.

Example:

```python
def show_welcome():
    print("Welcome to Track Career Analyzer")
```

The function does not run until you call it:

```python
show_welcome()
```

### Function Call

A function call tells Python to run a function.

Example:

```python
show_welcome()
```

### Parameter

A parameter is information a function receives.

Example:

```python
def display_result(result):
    print(result)
```

Here, `result` is the parameter.

### Argument

An argument is the actual value you pass into a function call.

Example:

```python
display_result(57.85)
```

Here, `57.85` is the argument.

### Return Value

A return value is information a function sends back.

Example:

```python
def calculate_best_result(results):
    return min(results)
```

The function receives a list and returns the best result.

### Single Responsibility

A function should usually have one clear job.

Good function job:

```text
Display all results
```

Too many jobs:

```text
Ask for profile information, collect results, compare goals, print summary, and save files
```

## Step 1: Start From `main`

Make sure your local `main` branch is up to date:

```bash
git switch main
git pull
```

Create your Phase 05 branch:

```bash
git switch -c phase-05-functions-clean-code
```

If the branch already exists, use:

```bash
git switch phase-05-functions-clean-code
```

Check:

```bash
git status
```

Expected idea: Git should say you are on branch `phase-05-functions-clean-code`.

## Step 2: Run The Current App

Run the app before changing it:

```bash
cd app
python3 app.py
cd ..
```

The goal of this phase is to keep the same behavior while organizing the code better.

## Step 3: Create A Welcome Function

Open:

```text
app/app.py
```

Move the welcome messages into a function:

```python
def show_welcome():
    print("Welcome to Track Career Analyzer")
    print("This app will grow throughout the Python bootcamp.")
```

Call the function:

```python
show_welcome()
```

Run the app.

Expected idea: the welcome messages should still print.

## Step 4: Create A Profile Function

Move the profile input code into a function:

```python
def get_athlete_profile():
    athlete_name = input("Athlete name: ")
    graduation_year = int(input("Graduation year: "))
    primary_event = input("Primary event: ")
    current_pr = float(input("Current PR: "))

    return athlete_name, graduation_year, primary_event, current_pr
```

Call it:

```python
athlete_name, graduation_year, primary_event, current_pr = get_athlete_profile()
```

This function returns multiple values. That is okay for this phase.

Run the app after this change.

## Step 5: Create A Profile Display Function

Move profile printing into a function:

```python
def display_athlete_profile(athlete_name, graduation_year, primary_event, current_pr):
    print()
    print("Athlete Profile")
    print("---------------")
    print(f"Name: {athlete_name}")
    print(f"Graduation year: {graduation_year}")
    print(f"Primary event: {primary_event}")
    print(f"Current PR: {current_pr}")
```

Call it:

```python
display_athlete_profile(athlete_name, graduation_year, primary_event, current_pr)
```

Explain out loud:

- What are the parameters?
- What values are passed in?
- Does this function return anything?

## Step 6: Create A Results Function

Move result collection into a function:

```python
def collect_results():
    results = []

    for number in range(3):
        result = float(input(f"Enter result #{number + 1}: "))
        results.append(result)

    return results
```

Call it:

```python
results = collect_results()
```

Run the app and confirm it still asks for three results.

## Step 7: Create A Results Display Function

Move result summary printing into a function:

```python
def display_results(results):
    print()
    print("Results Summary")
    print("---------------")

    for result in results:
        print(result)

    print(f"Number of results: {len(results)}")
    print(f"Best result: {min(results)}")
```

Call it:

```python
display_results(results)
```

This function receives the list as a parameter.

## Step 8: Create A Best Result Function

Move best result calculation into a function:

```python
def calculate_best_result(results):
    return min(results)
```

Then update the display function:

```python
def display_results(results):
    print()
    print("Results Summary")
    print("---------------")

    for result in results:
        print(result)

    best_result = calculate_best_result(results)

    print(f"Number of results: {len(results)}")
    print(f"Best result: {best_result}")
```

Explain out loud:

- What goes into `calculate_best_result()`?
- What comes back?
- Why does this function use `return`?

## Step 9: Create A Goal Comparison Function

Move goal comparison into a function:

```python
def compare_to_goal(current_pr, goal_mark):
    difference = current_pr - goal_mark

    if current_pr < goal_mark:
        print("Goal reached!")
    elif current_pr == goal_mark:
        print("Exactly at the goal!")
    else:
        print("Still chasing the goal.")
        print(f"Difference: {difference} seconds")
```

Call it:

```python
goal_mark = float(input("Goal mark: "))
compare_to_goal(current_pr, goal_mark)
```

Run the app and test the three goal paths again:

- Faster than goal
- Exactly at goal
- Still chasing

## Step 10: Organize The Bottom Of The File

At the bottom of the file, the main flow might look like this:

```python
show_welcome()
athlete_name, graduation_year, primary_event, current_pr = get_athlete_profile()
display_athlete_profile(athlete_name, graduation_year, primary_event, current_pr)
goal_mark = float(input("Goal mark: "))
compare_to_goal(current_pr, goal_mark)
results = collect_results()
display_results(results)
```

Read those lines like a story.

If the function names are clear, the bottom of the file should be easier to understand than one long block of code.

## Step 11: Practice A Function Mistake

This step is optional but useful.

Temporarily call a function before it is defined:

```python
show_welcome()

def show_welcome():
    print("Welcome")
```

Run the app.

Python should show a `NameError`.

Read the error, then fix the code by defining functions before calling them.

Do not commit broken code.

## Step 12: Create Your Phase Reflection

Create:

```text
reflections/phase-05-reflection.md
```

Use the template from:

```text
reflections/phase-reflection-template.md
```

Fill in short answers for:

- What a function is
- What a function call is
- What a parameter is
- What a return value is
- Which function you understand best
- One error or mistake you saw
- Whether you used AI

## Step 13: Check Your Work With Git

From the main repository folder, run:

```bash
git status
```

You should normally see:

```text
app/app.py
reflections/phase-05-reflection.md
```

Review the code change:

```bash
git diff app/app.py
```

## Step 14: Commit And Push

Stage only the Phase 05 files:

```bash
git add app/app.py reflections/phase-05-reflection.md
```

Commit:

```bash
git commit -m "Complete phase 05 functions"
```

Push:

```bash
git push -u origin phase-05-functions-clean-code
```

## Step 15: Open A Pull Request

Open a pull request from:

```text
phase-05-functions-clean-code -> main
```

Fill out the pull request template.

In the AI disclosure, include any prompt you used to understand functions, parameters, return values, refactoring, or error messages.

## Common Stuck Points

### The function does not run

Defining a function is not the same as calling it.

This defines the function:

```python
def show_welcome():
    print("Welcome")
```

This calls it:

```python
show_welcome()
```

### `NameError`

Python cannot find the function or variable name.

Check:

- Is the function defined before it is called?
- Is the name spelled the same way?
- Did you use parentheses when calling the function?

### Confusing parameter and argument

Parameter: the name in the function definition.

```python
def display_result(result):
```

Argument: the actual value passed into the function.

```python
display_result(57.85)
```

### Return value disappears

If a function returns a value, store it:

```python
results = collect_results()
```

If you only call the function without storing the return value, the program may lose the information.

### Too many functions too fast

Refactor one piece at a time.

After each function, run the app.

## AI Guidelines For This Phase

Good AI prompts:

```text
I am in Phase 05. Explain the difference between a parameter and an argument using my function.
```

```text
I got a NameError after moving code into a function. Explain the clue, but do not rewrite my whole program.
```

```text
Ask me questions to check whether I understand return values.
```

Avoid prompts like:

```text
Refactor my whole Phase 05 program into functions for me.
```

## Demo

Show:

- `app/app.py` in VS Code.
- The app running in Terminal.
- The bottom of the file where the main flow calls functions.
- One function that has parameters.
- One function that returns a value.
- Your Phase 05 reflection.

Explain:

- What a function is.
- What a function call is.
- What a parameter is.
- What a return value is.
- Why functions make code easier to read.
- One error or mistake you saw.
- How AI helped, if you used it.

Live change:

- Change the number of results collected from three to four.
- Save the file.
- Run the app again.
- Explain which function changed.

## Good Enough To Move On

You are ready for Phase 06 when:

- You can run the refactored app.
- You can explain at least three functions.
- You can explain one parameter.
- You can explain one return value.
- You can make one small function change without AI.
- You committed and pushed your Phase 05 work.
- You opened a pull request and completed the AI disclosure.

