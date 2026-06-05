# Phase 02 Review Checklist

Use this checklist while reviewing the student's Phase 02 pull request and demo.

## Expected Deliverables

The student should update:

```text
app/app.py
reflections/phase-02-reflection.md
```

`app/app.py` should ask for an athlete profile using `input()` and print a formatted summary. Keep expectations beginner-level. Do not expect functions, loops, file saving, pandas, or Streamlit yet.

## Commands The Student Should Be Able To Run

```bash
git switch main
git pull
git switch -c phase-02-athlete-profile
cd app
python3 app.py
cd ..
git status
git diff app/app.py
git add app/app.py reflections/phase-02-reflection.md
git commit -m "Complete phase 02 athlete profile"
git push -u origin phase-02-athlete-profile
```

The student does not need to have every command memorized, but should understand the main flow.

## Questions To Ask

- What is a variable?
- What variable names did you choose?
- What does `input()` do?
- Why does `input()` return text?
- What does `int()` do?
- What does `float()` do?
- What is an f-string?
- What happened when you typed a non-number for a numeric field?
- What changed in this pull request?
- Did you use AI? What did it help you understand?

## Common Mistakes To Watch For

- Student cannot explain why `input()` returns text.
- Student uses `int()` for a decimal PR and gets stuck.
- Student includes units like `57.85 seconds` in a `float()` input.
- Student has mismatched variable names.
- Student jumps ahead into conditionals, loops, or functions too early.
- Student cannot explain code that AI helped write.

## Good Enough To Move On

Move on when the student can:

- Run the program and enter a profile.
- Explain each variable in the file.
- Explain `input()` in plain language.
- Explain one type conversion.
- Make one small profile field change live without AI.
- Show a Phase 02 reflection.
- Explain the pull request at a high level.

## Suggested Feedback Language

```text
You are ready for Phase 03 because you can collect input, store it in variables, and explain the difference between text and numbers.
```

```text
Before moving on, let's practice why current_pr needs float() instead of leaving it as text.
```

```text
Keep this simple for now. Conditionals and goal comparisons are the focus of Phase 03.
```

