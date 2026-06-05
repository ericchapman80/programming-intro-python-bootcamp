# Phase 01 Review Checklist

Use this checklist while reviewing the student's Phase 01 pull request and demo.

## Expected Deliverables

The student should update:

```text
app/app.py
reflections/phase-01-reflection.md
```

`app/app.py` should still be simple. It should use `print()` statements only. Do not expect variables, input, functions, pandas, or Streamlit yet.

## Commands The Student Should Be Able To Run

```bash
git switch main
git pull
git switch -c phase-01-first-python
cd app
python3 app.py
cd ..
git status
git diff app/app.py
git add app/app.py reflections/phase-01-reflection.md
git commit -m "Complete phase 01 first Python program"
git push -u origin phase-01-first-python
```

The student does not need to have every command memorized, but should understand what the main commands are doing.

## Questions To Ask

- What file did you edit?
- What makes this a Python file?
- What does `print()` do?
- What is the text inside quotation marks called?
- What command runs the app?
- What folder do you need to be in when running `python3 app.py`?
- What error did you see or intentionally test?
- What changed in this pull request?
- Did you use AI? What did it help you understand?

## Common Mistakes To Watch For

- Student runs `python3 app.py` from the wrong folder.
- Student forgets to save the file before running it.
- Student commits generated or unrelated files.
- Student cannot explain the text they added.
- Student uses AI to write a reflection they cannot explain.
- Student jumps ahead into variables, input, or functions too early.

## Good Enough To Move On

Move on when the student can:

- Run the app from Terminal.
- Explain every line in `app/app.py`.
- Make one small print-message change live without AI.
- Read a simple syntax error with coaching.
- Show a Phase 01 reflection.
- Explain the pull request at a high level.

## Suggested Feedback Language

```text
You are ready for Phase 02 because you can run the app, explain print(), and make a small change yourself.
```

```text
Before moving on, let's practice running the app from the correct folder one more time.
```

```text
Keep the code simple in Phase 01. Variables and input are coming next.
```

