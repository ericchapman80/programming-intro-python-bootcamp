# Phase 04 Review Checklist

Use this checklist while reviewing the student's Phase 04 pull request and demo.

## Expected Deliverables

The student should update:

```text
app/app.py
reflections/phase-04-reflection.md
```

`app/app.py` should collect multiple results into a list, display them with a loop, count them, and show the best result for a timed event. Keep expectations beginner-level. Do not expect functions, file saving, pandas, Streamlit, or flexible event-specific scoring yet.

## Commands The Student Should Be Able To Run

```bash
git switch main
git pull
git switch -c phase-04-lists-loops-results
cd app
python3 app.py
cd ..
git status
git diff app/app.py
git add app/app.py reflections/phase-04-reflection.md
git commit -m "Complete phase 04 lists and loops"
git push -u origin phase-04-lists-loops-results
```

The student does not need to have every command memorized, but should understand the main flow.

## Questions To Ask

- What is a list?
- What is one item in your results list?
- What does `append()` do?
- What does the `for` loop repeat?
- What does `range(3)` mean?
- Why does the prompt use `number + 1`?
- What does `len()` do?
- Why does `min()` find the best result for timed events?
- What changed in this pull request?
- Did you use AI? What did it help you understand?

## Common Mistakes To Watch For

- Student cannot explain the difference between `result` and `results`.
- Student calls `append()` on the wrong variable.
- Student thinks `range(3)` counts `1, 2, 3`.
- Student only prints the list directly and does not loop through it.
- Student uses `max()` for timed events without explaining why.
- Student adds functions or file saving too early.
- Student cannot explain code that AI helped write.

## Good Enough To Move On

Move on when the student can:

- Run the app and enter multiple results.
- Explain the results list.
- Explain the loop that collects or displays results.
- Explain `append()`, `len()`, and `min()`.
- Make one small loop-count change live without AI.
- Show a Phase 04 reflection.
- Explain the pull request at a high level.

## Suggested Feedback Language

```text
You are ready for Phase 05 because you can store multiple results, loop through them, and explain how the best timed result is found.
```

```text
Before moving on, let's trace the loop one result at a time.
```

```text
Keep the repeated code visible for now. Phase 05 will organize it into functions.
```

