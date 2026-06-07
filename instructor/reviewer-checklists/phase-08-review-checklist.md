# Phase 08 Review Checklist

Use this checklist while reviewing the student's Phase 08 pull request and demo.

## Expected Deliverables

The student should add or update:

```text
app/streamlit_app.py
reflections/phase-08-reflection.md
```

The student may also update:

```text
app/data/results.csv
```

`streamlit_app.py` should run locally, load CSV data, display a table, filter one event, show at least one metric, and show a simple chart. Keep expectations beginner-level. Do not expect deployment, authentication, databases, advanced styling, or a polished production app yet.

## Commands The Student Should Be Able To Run

```bash
git switch main
git pull
git switch -c phase-08-streamlit-app
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python -m pip show streamlit
cd app
streamlit run streamlit_app.py
python3 -m streamlit run streamlit_app.py
cd ..
git status
git diff app/streamlit_app.py
git add app/streamlit_app.py reflections/phase-08-reflection.md
git commit -m "Complete phase 08 Streamlit app"
git push -u origin phase-08-streamlit-app
```

The student does not need to have every command memorized, but should understand the main flow.

## Questions To Ask

- What is Streamlit?
- What does localhost mean?
- How is this different from running `python3 app.py`?
- What data file does the app load?
- What widget did you use?
- What pandas calculation powers one metric?
- What does the chart show?
- Why might lower marks look like improvement going downward?
- What changed in this pull request?
- Did you use AI? What did it help you understand?

## Common Mistakes To Watch For

- Student runs `python3 streamlit_app.py` instead of `streamlit run streamlit_app.py`.
- Student runs Streamlit from the wrong folder and hits file path issues.
- Student cannot explain localhost.
- Student adds too much styling or complexity too early.
- Student cannot explain the pandas calculation behind a metric.
- Student copies Streamlit code from AI without being able to explain it.

## Good Enough To Move On

Move on when the student can:

- Run the Streamlit app locally.
- Open it in a browser.
- Explain localhost.
- Display CSV data.
- Filter one event.
- Show one metric and one chart.
- Make one small UI text change live without AI.
- Show a Phase 08 reflection.
- Explain the pull request at a high level.

## Suggested Feedback Language

```text
You are ready for Phase 09 because you can run the app in a browser, explain localhost, and show data-driven metrics from the CSV.
```

```text
Before moving on, let's trace one value from the CSV into the table, metric, and chart.
```

```text
Keep the app simple for now. Deployment and sharing are the focus of Phase 09.
```
