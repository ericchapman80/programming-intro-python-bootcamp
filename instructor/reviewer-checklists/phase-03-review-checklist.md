# Phase 03 Review Checklist

Use this checklist while reviewing the student's Phase 03 pull request and demo.

## Expected Deliverables

The student should update:

```text
app/app.py
reflections/phase-03-reflection.md
```

`app/app.py` should compare a current mark to a goal mark using `if`, `elif`, and `else`. Keep expectations beginner-level. Do not expect functions, loops, file saving, pandas, Streamlit, or event-specific mark parsing yet.

## Commands The Student Should Be Able To Run

```bash
git switch main
git pull
git switch -c phase-03-goal-conditionals
cd app
python3 app.py
cd ..
git status
git diff app/app.py
git add app/app.py reflections/phase-03-reflection.md
git commit -m "Complete phase 03 goal conditionals"
git push -u origin phase-03-goal-conditionals
```

The student does not need to have every command memorized, but should understand the main flow.

## Questions To Ask

- What is a conditional?
- What does the `if` line check?
- What does `elif` mean?
- When does `else` run?
- What is a Boolean?
- What comparison operators did you use?
- Why does lower mean better for this phase's running examples?
- What happened when you tested faster, equal, and still-chasing cases?
- What changed in this pull request?
- Did you use AI? What did it help you understand?

## Common Mistakes To Watch For

- Student uses `=` instead of `==` for equality checks.
- Student forgets indentation under `if`, `elif`, or `else`.
- Student reverses the comparison for running times.
- Student only tests one path.
- Student adds advanced event-specific logic too early.
- Student cannot explain code that AI helped write.

## Good Enough To Move On

Move on when the student can:

- Run the app and enter a current mark and goal mark.
- Explain the `if` / `elif` / `else` block.
- Explain one comparison operator.
- Test faster, equal, and still-chasing cases.
- Make one small message change live without AI.
- Show a Phase 03 reflection.
- Explain the pull request at a high level.

## Suggested Feedback Language

```text
You are ready for Phase 04 because you can make the program choose different messages based on the goal comparison.
```

```text
Before moving on, let's test all three paths again and explain why each one ran.
```

```text
Keep the running-time rule simple for now. Lists and multiple results are the focus of Phase 04.
```

