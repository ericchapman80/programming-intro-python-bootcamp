# Phase 06 Review Checklist

Use this checklist while reviewing the student's Phase 06 pull request and demo.

## Expected Deliverables

The student should update:

```text
app/app.py
app/data/results.csv
reflections/phase-06-reflection.md
```

`app/app.py` should read saved results from `app/data/results.csv`, add a new result, save it, and display saved results. Keep expectations beginner-level. Do not expect pandas, Streamlit, databases, advanced validation, or a polished menu yet.

## Commands The Student Should Be Able To Run

```bash
git switch main
git pull
git switch -c phase-06-csv-persistence
cd app
python3 app.py
cd ..
git status
git diff app/app.py
git diff app/data/results.csv
git add app/app.py app/data/results.csv reflections/phase-06-reflection.md
git commit -m "Complete phase 06 CSV persistence"
git push -u origin phase-06-csv-persistence
```

The student does not need to have every command memorized, but should understand the main flow.

## Questions To Ask

- What does persistence mean?
- What is a CSV file?
- What does the header row do?
- What file path does the app use?
- What does `load_results()` do?
- What does `save_result()` do?
- Why does the app use append mode?
- What happened when you ran the app a second time?
- What changed in this pull request?
- Did you use AI? What did it help you understand?

## Common Mistakes To Watch For

- Student runs the app from the wrong folder and hits file path issues.
- Student deletes the CSV header row.
- Student duplicates the header row while appending.
- Student writes rows on odd lines because `newline=""` is missing.
- Student expects pandas-style analysis too early.
- Student cannot explain code that AI helped write.

## Good Enough To Move On

Move on when the student can:

- Run the app and save a result.
- Show the saved row in `app/data/results.csv`.
- Run the app again and see saved data.
- Explain persistence and the CSV header row.
- Explain `load_results()` and `save_result()` in plain language.
- Make one small CSV edit live without AI.
- Show a Phase 06 reflection.
- Explain the pull request at a high level.

## Suggested Feedback Language

```text
You are ready for Phase 07 because your app can save results, reload them, and you can explain how the CSV file stores data.
```

```text
Before moving on, let's trace one result from Terminal input into the CSV row.
```

```text
Keep the storage simple for now. Pandas analysis is the focus of Phase 07.
```

