# Phase 07 Review Checklist

Use this checklist while reviewing the student's Phase 07 pull request and demo.

## Expected Deliverables

The student should update:

```text
app/app.py
app/data/results.csv
reflections/phase-07-reflection.md
```

`app/app.py` should load saved CSV data with pandas and calculate at least one useful statistic. Keep expectations beginner-level. Do not expect charts, Streamlit, deployment, advanced cleaning, or professional analytics yet.

## Commands The Student Should Be Able To Run

```bash
git switch main
git pull
git switch -c phase-07-pandas-analysis
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python -m pip show pandas
cd app
python3 app.py
cd ..
git status
git diff app/app.py
git diff app/data/results.csv
git add app/app.py app/data/results.csv reflections/phase-07-reflection.md
git commit -m "Complete phase 07 pandas analysis"
git push -u origin phase-07-pandas-analysis
```

The student does not need to have every command memorized, but should understand the main flow.

## Questions To Ask

- What is pandas?
- What is a DataFrame?
- How is a DataFrame like a spreadsheet?
- What are rows and columns in your CSV?
- Why did `mark` need numeric conversion?
- What does filtering do?
- What does `groupby()` do in your own words?
- What statistic did you calculate?
- What insight did you find?
- What changed in this pull request?
- Did you use AI? What did it help you understand?

## Common Mistakes To Watch For

- Student has pandas installed in a different Python environment.
- Student runs the app from the wrong folder and hits file path issues.
- Student cannot explain DataFrame vs CSV file.
- Student forgets to convert `mark` to numeric before stats.
- Student treats different events as directly comparable without caveat.
- Student copies pandas code from AI without being able to explain it.

## Good Enough To Move On

Move on when the student can:

- Load `results.csv` into a DataFrame.
- Explain the DataFrame using a spreadsheet analogy.
- Filter one event.
- Calculate at least one statistic.
- Explain one insight from the saved data.
- Add one CSV row and rerun the analysis live without AI.
- Show a Phase 07 reflection.
- Explain the pull request at a high level.

## Suggested Feedback Language

```text
You are ready for Phase 08 because you can load saved results with pandas, filter the data, and explain at least one statistic.
```

```text
Before moving on, let's trace one CSV row into the DataFrame and then into your statistic.
```

```text
Keep the analysis simple. Phase 08 will focus on making this visible in a Streamlit app.
```
