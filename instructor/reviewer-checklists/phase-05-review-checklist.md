# Phase 05 Review Checklist

Use this checklist while reviewing the student's Phase 05 pull request and demo.

## Expected Deliverables

The student should update:

```text
app/app.py
reflections/phase-05-reflection.md
```

`app/app.py` should be refactored into beginner-friendly functions. Keep expectations simple. Do not expect classes, modules, tests, file saving, pandas, or Streamlit yet.

## Commands The Student Should Be Able To Run

```bash
git switch main
git pull
git switch -c phase-05-functions-clean-code
cd app
python3 app.py
cd ..
git status
git diff app/app.py
git add app/app.py reflections/phase-05-reflection.md
git commit -m "Complete phase 05 functions"
git push -u origin phase-05-functions-clean-code
```

The student does not need to have every command memorized, but should understand the main flow.

## Questions To Ask

- What is a function?
- What is a function call?
- What function do you understand best?
- What does this function receive?
- What does this function return?
- What is the difference between a parameter and an argument?
- Why did you move this code into a function?
- What changed in this pull request?
- Did you use AI? What did it help you understand?

## Common Mistakes To Watch For

- Student defines a function but forgets to call it.
- Student calls a function before defining it.
- Student loses returned values by not storing them.
- Student cannot explain parameters.
- Student creates too many functions without understanding them.
- Student uses advanced patterns or classes too early.
- Student cannot explain code that AI helped write.

## Good Enough To Move On

Move on when the student can:

- Run the refactored app.
- Explain at least three functions.
- Explain one parameter.
- Explain one return value.
- Make one small function change live without AI.
- Show a Phase 05 reflection.
- Explain the pull request at a high level.

## Suggested Feedback Language

```text
You are ready for Phase 06 because you can organize code into functions and explain what information moves in and out.
```

```text
Before moving on, let's trace this function call from the bottom of the file back to the function definition.
```

```text
Keep the functions simple. File saving is the focus of Phase 06.
```

