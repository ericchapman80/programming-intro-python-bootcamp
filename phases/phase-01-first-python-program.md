# Phase 01: First Python Program

## Goal

Run and edit your first Python program.

By the end of this phase, you should be able to open `app/app.py`, explain what `print()` does, run the program from Terminal, make a small change, commit it, push it, and open a pull request.

> [!TIP]
> Your first win is simple: make Python say something, then change what it says.

## At A Glance

| You will | What it proves |
| --- | --- |
| Open `app/app.py` | You can find code in the repo |
| Run `python3 app.py` | You can execute Python |
| Edit a `print()` message | You can change program output |
| Read one error | Bugs are clues, not dead ends |
| Open a PR | Your code change has a review path |

## Why This Phase Matters

This is the first time you change code in the Track Career Analyzer app.

The app is tiny right now on purpose. Professional software starts the same way: make something small run, then improve it one step at a time.

## Time Estimate

Plan for 60-90 minutes.

Take your time reading the file and running the command more than once.

## Before You Start

You should have completed Phase 00 or be able to:

- Open Terminal.
- Navigate to the repository folder.
- Open the project in VS Code.
- Run `git status`.
- Explain what a branch is.

You do not need to know Python yet.

## New Concepts

### Python File

A Python file usually ends in `.py`.

This project starts with:

```text
app/app.py
```

That file contains Python code.

### `print()`

`print()` tells Python to show text in Terminal.

Example:

```python
print("Welcome to Track Career Analyzer")
```

The text inside the quotation marks is called a string.

### Syntax

Syntax means the rules for how code must be written.

This works:

```python
print("Hello")
```

This does not work:

```python
print("Hello)
```

The second example is missing a closing quotation mark.

### Error Message

An error message is Python giving you a clue about what went wrong.

> [!IMPORTANT]
> Do not memorize error messages. Learn to slow down and find the file name, line number, and clue.

Do not panic when you see one. Read it slowly.

## Step 1: Start From `main`

Before starting a phase, make sure you are on `main` and up to date.

```bash
git switch main
git pull
```

Create your Phase 01 branch:

```bash
git switch -c phase-01-first-python
```

Check where you are:

```bash
git status
```

Expected idea: Git should say you are on branch `phase-01-first-python`.

If the branch already exists, use:

```bash
git switch phase-01-first-python
```

## Step 2: Open The App File

Open this file in VS Code:

```text
app/app.py
```

Read it out loud.

It should currently be short, something like:

```python
print("Welcome to Track Career Analyzer")
print("This app will grow throughout the Python bootcamp.")
```

## Step 3: Run The Program

In Terminal, go into the `app` folder:

```bash
cd app
```

Run the program:

```bash
python3 app.py
```

Expected output:

```text
Welcome to Track Career Analyzer
This app will grow throughout the Python bootcamp.
```

If it runs, you have executed your first Python program in this bootcamp.

## Step 4: Return To The Repository Folder

After running the app from inside `app`, move back to the main repository folder:

```bash
cd ..
```

Check:

```bash
pwd
```

Expected idea: the path should end with:

```text
programming-intro-python-bootcamp
```

## Step 5: Make A Small Code Change

In `app/app.py`, add one more printed line.

Example:

```python
print("Phase 01 is about running and editing Python code.")
```

Save the file.

Run the program again:

```bash
cd app
python3 app.py
cd ..
```

You should see your new line in the output.

## Step 6: Practice Reading An Error

This step is optional but useful.

> [!WARNING]
> Break the code only for practice, then fix it before committing. Never commit code you already know is broken.

Temporarily break one line by removing a closing quotation mark:

```python
print("Welcome to Track Career Analyzer)
```

Run:

```bash
cd app
python3 app.py
cd ..
```

Python should show an error.

Read the error message. Look for:

- The file name
- The line number
- The kind of error
- The arrow or highlighted location

Fix the line immediately after reading the error.

Run the program again to confirm it works.

Do not commit broken code.

## Step 7: Create Your Phase Reflection

Create:

```text
reflections/phase-01-reflection.md
```

Use the template from:

```text
reflections/phase-reflection-template.md
```

Fill in short answers for:

- What you built
- What `print()` does
- What command runs the app
- One error or mistake you saw
- Whether you used AI
- What live demo change you will make

## Step 8: Check Your Work With Git

From the main repository folder, run:

```bash
git status
```

You should see changes to:

```text
app/app.py
reflections/phase-01-reflection.md
```

Look at the code change:

```bash
git diff app/app.py
```

## Step 9: Commit And Push

Stage only the Phase 01 files:

```bash
git add app/app.py reflections/phase-01-reflection.md
```

Commit:

```bash
git commit -m "Complete phase 01 first Python program"
```

Push:

```bash
git push -u origin phase-01-first-python
```

## Step 10: Open A Pull Request

Open a pull request from:

```text
phase-01-first-python -> main
```

Fill out the pull request template.

Be specific about AI usage. If you used AI to understand an error message, say what you asked and what you learned.

## Optional Level-Up: AI Assistant Setup 🤖

Do this only after the main Phase 01 work is running, committed, pushed, and opened as a pull request.

The first Python win should be manual: open the file, run it, change it, commit it, and explain it yourself. After that, it is reasonable to set up an AI assistant as a coach.

> [!TIP]
> This is optional. If setup starts to feel like a distraction, skip it and keep moving to Phase 02.

### Option 1: ChatGPT As A Tutor

Use ChatGPT in the browser or app for explanations, hints, and review questions.

Good uses:

- Explain a Python error message.
- Ask quiz questions about `print()`, strings, and Terminal commands.
- Help rewrite a confusing reflection sentence in Riley's own words.
- Review a small code snippet for readability.

Avoid:

- Asking for the full Phase 01 solution.
- Asking AI to write the reflection from scratch.
- Copying code you cannot explain.

### Option 2: One Coding Assistant

If the family wants an IDE or coding assistant, pick one tool to try first.

Examples include:

- OpenAI Codex in an IDE, CLI, app, or web workflow.
- GitHub Copilot in VS Code.
- Specialized AI IDEs such as Cursor or Windsurf.
- Other command-line assistants.

The specific choice depends on the account you already have, comfort level, privacy settings, cost, and how much help feels useful instead of distracting.

Read:

- [AI Guidelines](../AI_GUIDELINES.md)
- [AI Tooling Landscape](../docs/ai-tooling-landscape.md)
- [AI Coaching Guide](../docs/ai-coaching-guide.md)

### Phase 01 AI Rules

- Ask for hints before code.
- Ask AI to explain errors, not erase them.
- Keep the final code small enough to explain.
- Say exactly how AI helped in the PR.
- Make the demo live change without AI.

## Common Stuck Points

### `python3 app.py` says file not found

You are probably in the wrong folder.

Run:

```bash
pwd
ls
```

If you are in the main repo folder, use:

```bash
cd app
python3 app.py
```

### Python shows `SyntaxError`

Check for:

- Missing quotation marks
- Missing parentheses
- Extra characters
- Curly quotes copied from a document instead of straight quotes

### The output did not change

Make sure you saved the file in VS Code.

Then run the program again.

### `git status` shows more files than expected

Pause before committing. Ask what changed and why.

For Phase 01, you should normally commit only:

```text
app/app.py
reflections/phase-01-reflection.md
```

## AI Guidelines For This Phase

Good AI prompts:

```text
I am in Phase 01. Explain what print() does using this line: print("Welcome")
```

```text
I got this Python error. Explain the clue, but do not rewrite the whole file.
```

```text
Ask me questions to check whether I understand how to run app.py.
```

Avoid prompts like:

```text
Write my Phase 01 code and reflection for me.
```

## Demo

Show:

- `app/app.py` in VS Code.
- Terminal open in the project.
- The command used to run the app.
- The app output.
- Your Phase 01 reflection.

Explain:

- What a `.py` file is.
- What `print()` does.
- What a string is.
- What command runs the app.
- One error or mistake you saw.
- How AI helped, if you used it.

Live change:

- Change one printed message without AI.
- Save the file.
- Run the app again.
- Explain why the output changed.

## Good Enough To Move On

You are ready for Phase 02 when:

- You can run `python3 app.py`.
- You can explain each line in `app/app.py`.
- You can make a small printed-message change.
- You can explain one syntax error or mistake.
- You committed and pushed your Phase 01 work.
- You opened a pull request and completed the AI disclosure.
