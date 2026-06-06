# Phase 04: Lists, Loops, and Multiple Results

## Goal

Use lists and loops to work with more than one track result.

By the end of this phase, you should be able to store multiple results in a list, loop through the list, count the results, and find the best result for a timed event.

## Why This Phase Matters

Real athletes do not have only one result.

In Phase 03, the app compared one current mark to one goal. In Phase 04, the app starts handling a season of results. This is a major programming step: moving from one value to many values.

## Time Estimate

Plan for 90-120 minutes.

Loops can feel strange at first. Test with a short list before adding repeated user input.

## Before You Start

You should be able to:

- Run `python3 app.py`.
- Explain variables.
- Use `input()`.
- Use `float()` for decimal marks.
- Explain `if`, `elif`, and `else`.
- Commit, push, and open a pull request.

## New Concepts

### List

A list stores multiple values in one variable.

Example:

```python
results = [58.20, 57.85, 57.30]
```

Think of a list like a row of boxes. Each box holds one result.

### Item

An item is one value inside a list.

In this list:

```python
results = [58.20, 57.85, 57.30]
```

`58.20` is one item.

### `append()`

`append()` adds a new item to the end of a list.

Example:

```python
results.append(57.10)
```

### `for` Loop

A `for` loop repeats code once for each item in a list.

Example:

```python
for result in results:
    print(result)
```

If the list has three results, the loop runs three times.

### `len()`

`len()` counts how many items are in a list.

Example:

```python
number_of_results = len(results)
```

### `min()` and `max()`

`min()` finds the smallest value.

`max()` finds the largest value.

For timed running events in this phase, lower is better, so `min()` finds the best result.

Example:

```python
best_result = min(results)
```

## Step 1: Start From `main`

Make sure your local `main` branch is up to date:

```bash
git switch main
git pull
```

Create your Phase 04 branch:

```bash
git switch -c phase-04-lists-loops-results
```

If the branch already exists, use:

```bash
git switch phase-04-lists-loops-results
```

Check:

```bash
git status
```

Expected idea: Git should say you are on branch `phase-04-lists-loops-results`.

## Step 2: Run The Current App

Run the app before changing it:

```bash
cd app
python3 app.py
cd ..
```

The app should collect profile and goal information from earlier phases.

## Step 3: Start With A Hard-Coded List

Open:

```text
app/app.py
```

Add a simple results list:

```python
results = [58.20, 57.85, 57.30]
```

Print the whole list:

```python
print(results)
```

Run the app.

This output may not be pretty yet. The goal is to prove the list exists.

## Step 4: Loop Through The Results

Replace the plain list print with a loop:

```python
print("Meet Results")
print("------------")

for result in results:
    print(result)
```

Run the app again.

Explain out loud:

- What is the list called?
- What is one item in the list?
- How many times does the loop run?
- What does `result` represent during each loop?

## Step 5: Count The Results

Add:

```python
number_of_results = len(results)
print(f"Number of results: {number_of_results}")
```

Run the app.

Expected idea: if your list has three items, the count should be `3`.

## Step 6: Find The Best Result

For timed running events, lower is better.

Add:

```python
best_result = min(results)
print(f"Best result: {best_result}")
```

Run the app.

Expected idea: from `[58.20, 57.85, 57.30]`, the best result should be:

```text
57.3
```

Python may print `57.3` instead of `57.30`. That is okay for now.

## Step 7: Add Results With `append()`

Start with an empty list:

```python
results = []
```

Append three results:

```python
results.append(58.20)
results.append(57.85)
results.append(57.30)
```

Run the app again.

The output should be the same as before. The code is now showing how a list can grow over time.

## Step 8: Ask The User For Results

Replace the hard-coded `append()` values with `input()`:

```python
results = []

first_result = float(input("First result: "))
second_result = float(input("Second result: "))
third_result = float(input("Third result: "))

results.append(first_result)
results.append(second_result)
results.append(third_result)
```

Run the app and enter three decimal times.

This is repeated code. That is acceptable for this phase because the goal is understanding lists first.

## Step 9: Use A Loop For Repeated Input

Once the three-input version works, replace it with a loop:

```python
results = []

for number in range(3):
    result = float(input("Enter result: "))
    results.append(result)
```

Run the app.

The prompt will appear three times.

Explain out loud:

- What starts empty?
- What gets added each time?
- How many times does the loop run?

## Step 10: Label The Result Number

Make the prompt clearer:

```python
for number in range(3):
    result = float(input(f"Enter result #{number + 1}: "))
    results.append(result)
```

`number + 1` is used because `range(3)` starts counting at `0`.

The prompts should look like:

```text
Enter result #1:
Enter result #2:
Enter result #3:
```

## Step 11: Display A Summary

After collecting the results, display:

- All results
- Number of results
- Best result

Example:

```python
print()
print("Results Summary")
print("---------------")

for result in results:
    print(result)

print(f"Number of results: {len(results)}")
print(f"Best result: {min(results)}")
```

Keep using `min()` for this phase because timed running events use lower-is-better logic.

## Step 12: Practice A List Mistake

This step is optional but useful.

Temporarily misspell the list name:

```python
result.append(result)
```

Run the app.

Python should show an error because `result` is a number, not the list.

Read the error, then fix the line:

```python
results.append(result)
```

Run the app again to confirm it works.

Do not commit broken code.

## Step 13: Create Your Phase Reflection

Create:

```text
reflections/phase-04-reflection.md
```

Use the template from:

```text
reflections/phase-reflection-template.md
```

Fill in short answers for:

- What a list is
- What `append()` does
- What a `for` loop does
- What `range(3)` means
- Why `min()` finds the best timed result
- One error or mistake you saw
- Whether you used AI

## Step 14: Check Your Work With Git

From the main repository folder, run:

```bash
git status
```

You should normally see:

```text
app/app.py
reflections/phase-04-reflection.md
```

Review the code change:

```bash
git diff app/app.py
```

## Step 15: Commit And Push

Stage only the Phase 04 files:

```bash
git add app/app.py reflections/phase-04-reflection.md
```

Commit:

```bash
git commit -m "Complete phase 04 lists and loops"
```

Push:

```bash
git push -u origin phase-04-lists-loops-results
```

## Step 16: Open A Pull Request

Open a pull request from:

```text
phase-04-lists-loops-results -> main
```

Fill out the pull request template.

In the AI disclosure, include any prompt you used to understand lists, loops, `range()`, `append()`, or error messages.

## Common Stuck Points

### The loop runs three times, but starts at zero

`range(3)` gives:

```text
0
1
2
```

That is why the prompt uses `number + 1`.

### `NameError`

Python cannot find a variable with that name.

Check spelling:

```python
results
result
```

Those are different names.

### `AttributeError` with `append`

Make sure you call `append()` on the list:

```python
results.append(result)
```

Not on the single number:

```python
result.append(result)
```

### `ValueError` appears again

The app still uses `float()`. Type only a number, such as:

```text
57.85
```

Do not type:

```text
57.85 seconds
```

### `min()` feels backwards

For timed running events, lower is better.

If the event is a jump or throw, higher would be better and `max()` might be the right tool. For Phase 04, stay with timed events.

## AI Guidelines For This Phase

Good AI prompts:

```text
I am in Phase 04. Explain what this loop does one line at a time.
```

```text
I got an AttributeError with append(). Explain the clue, but do not rewrite my whole program.
```

```text
Ask me questions to check whether I understand lists and loops.
```

Avoid prompts like:

```text
Write the complete Phase 04 lists and loops program for me.
```

## Demo

Show:

- `app/app.py` in VS Code.
- The app running in Terminal.
- Three results entered through repeated input.
- The printed results summary.
- The best result.
- Your Phase 04 reflection.

Explain:

- What a list is.
- What one item in the list is.
- What `append()` does.
- What the `for` loop does.
- Why `range(3)` runs three times.
- Why `min()` finds the best timed result.
- One error or mistake you saw.
- How AI helped, if you used it.

Live change:

- Change the program to ask for four results instead of three.
- Save the file.
- Run the app again.
- Explain what code changed.

## Good Enough To Move On

You are ready for Phase 05 when:

- You can collect multiple results into a list.
- You can explain the loop that adds results.
- You can display every result using a loop.
- You can explain `len()` and `min()`.
- You can make one small loop-count change without AI.
- You committed and pushed your Phase 04 work.
- You opened a pull request and completed the AI disclosure.

