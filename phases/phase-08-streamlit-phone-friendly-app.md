# Phase 08: Streamlit Phone-Friendly App

## Goal

Turn Track Career Analyzer into a simple Streamlit web app that runs in a browser.

By the end of this phase, you should be able to create `streamlit_app.py`, run it locally, display saved CSV results, show simple pandas statistics, add a chart, and explain the difference between a terminal app and a browser-based app.

## Why This Phase Matters

The app has already learned how to collect data, save data, and analyze data.

Phase 08 makes that work easier to see and demo. Streamlit lets Python create a web app without learning HTML, CSS, JavaScript, React, or backend servers yet.

The goal is not a polished professional product. The goal is a clear, phone-friendly first app.

## Time Estimate

Plan for 2-3 hours.

Streamlit has a new run command and opens in a browser, so expect a few setup questions.

## Before You Start

You should be able to:

- Run `python3 app.py`.
- Explain pandas and DataFrames.
- Load `app/data/results.csv`.
- Calculate at least one statistic.
- Explain local files vs GitHub.
- Commit, push, and open a pull request.

## New Concepts

### Web App

A web app runs in a browser.

In this phase, the app still runs on your MacBook, but you view it in a browser tab.

### Streamlit

Streamlit is a Python library for building simple web apps.

Import it like this:

```python
import streamlit as st
```

The nickname `st` is a common convention.

### Localhost

Localhost means your own computer.

When Streamlit starts, it usually opens a URL like:

```text
http://localhost:8501
```

That means the app is running locally on your MacBook.

### Widget

A widget is an interactive control in the app.

Examples:

- Text input
- Select box
- Button
- Checkbox

### Metric

A metric is a small display for one important number.

Example:

```python
st.metric("Best mark", best_mark)
```

### Chart

A chart turns data into a visual.

For this phase, keep the chart simple.

## Step 1: Start From `main`

Make sure your local `main` branch is up to date:

```bash
git switch main
git pull
```

Create your Phase 08 branch:

```bash
git switch -c phase-08-streamlit-app
```

If the branch already exists, use:

```bash
git switch phase-08-streamlit-app
```

Check:

```bash
git status
```

Expected idea: Git should say you are on branch `phase-08-streamlit-app`.

## Step 2: Confirm Streamlit Is Available

From the repository root, run:

```bash
python3 -m pip show streamlit
```

If Streamlit is not installed, install requirements:

```bash
python3 -m pip install -r requirements.txt
```

Then check again:

```bash
python3 -m pip show streamlit
```

## Step 3: Create The Streamlit File

Create:

```text
app/streamlit_app.py
```

Start with:

```python
import pandas as pd
import streamlit as st

DATA_FILE = "data/results.csv"

st.set_page_config(
    page_title="Track Career Analyzer",
    layout="centered",
)

st.title("Track Career Analyzer")
st.write("Analyze saved track results from a CSV file.")
```

## Step 4: Run The Streamlit App

From the repository root:

```bash
cd app
streamlit run streamlit_app.py
```

Streamlit should open a browser tab.

If it does not open automatically, look for a local URL in Terminal, such as:

```text
http://localhost:8501
```

Open that URL in your browser.

To stop the app, click Terminal and press:

```text
Control-C
```

## Step 5: Load CSV Data

Add a function:

```python
def load_results():
    return pd.read_csv(DATA_FILE)
```

Then load the data:

```python
results = load_results()
```

Display it:

```python
st.subheader("Results")
st.dataframe(results, use_container_width=True)
```

Refresh the browser or let Streamlit rerun automatically.

You should see a table.

## Step 6: Handle An Empty CSV

If `results.csv` only has a header row, the app may not have useful data.

Add a simple check:

```python
if results.empty:
    st.info("No results yet. Add rows to data/results.csv.")
    st.stop()
```

This prevents the rest of the app from trying to analyze missing data.

## Step 7: Convert Marks To Numbers

Add:

```python
results["mark"] = pd.to_numeric(results["mark"])
```

If this fails, check `results.csv` for values like:

```text
57.85 seconds
```

For this phase, use plain numbers:

```text
57.85
```

## Step 8: Add A Profile Section

Add simple display values:

```python
st.subheader("Athlete Profile")

athlete_name = st.text_input("Athlete name", "Riley")
primary_event = st.text_input("Primary event", "400m")

st.write(f"{athlete_name} is analyzing results for {primary_event}.")
```

This is not permanent saved profile data yet. It is a simple Streamlit input practice.

## Step 9: Add Event Filter

Add:

```python
events = sorted(results["event"].unique())
selected_event = st.selectbox("Event", events)

event_results = results[results["event"] == selected_event]
```

This lets the user choose one event from the CSV.

## Step 10: Add Metrics

For timed events, lower is better.

Add:

```python
best_mark = event_results["mark"].min()
average_mark = event_results["mark"].mean()
result_count = len(event_results)

st.subheader("Event Summary")

st.metric("Best mark", best_mark)
st.metric("Average mark", round(average_mark, 2))
st.metric("Number of results", result_count)
```

Run the app and choose different events.

Explain out loud:

- What is being filtered?
- Why does `min()` mean best for timed events?
- What does each metric show?

## Step 11: Add Goal Progress

Add:

```python
goal_mark = st.number_input("Goal mark", min_value=0.0, value=float(best_mark), step=0.01)

if best_mark < goal_mark:
    st.success("Goal reached!")
elif best_mark == goal_mark:
    st.info("Exactly at the goal.")
else:
    difference = best_mark - goal_mark
    st.warning(f"Still chasing. Difference: {round(difference, 2)}")
```

Test:

- Goal slower than best mark
- Goal equal to best mark
- Goal faster than best mark

## Step 12: Add A Simple Chart

Add:

```python
chart_data = event_results[["date", "mark"]].set_index("date")
st.line_chart(chart_data)
```

This chart is intentionally simple.

The x-axis uses date. The y-axis uses mark.

For timed events, lower is better, so improvement may appear as the line going down.

## Step 13: Make It Phone-Friendly

Streamlit handles much of the responsive layout automatically.

Keep the layout simple:

- Use `layout="centered"`.
- Use clear section headers.
- Avoid wide side-by-side layouts.
- Prefer one column on small screens.
- Keep chart and table labels short.

Do not overdesign this phase.

## Step 14: Keep The Main File Readable

The Streamlit file might follow this order:

1. Imports and constants
2. Page config
3. Data loading function
4. Title
5. Load data
6. Empty data check
7. Profile inputs
8. Event filter
9. Table
10. Metrics
11. Goal progress
12. Chart

That is enough structure for Phase 08.

## Step 15: Practice A Streamlit Mistake

This step is optional but useful.

Temporarily run the app with Python:

```bash
python3 streamlit_app.py
```

You may see a warning that Streamlit apps should be run with:

```bash
streamlit run streamlit_app.py
```

Stop and restart the correct way.

## Step 16: Create Your Phase Reflection

Create:

```text
reflections/phase-08-reflection.md
```

Use the template from:

```text
reflections/phase-reflection-template.md
```

Fill in short answers for:

- What Streamlit is
- What localhost means
- How a terminal app differs from a browser app
- What widget you used
- What metric or chart you created
- One error or mistake you saw
- Whether you used AI

## Step 17: Check Your Work With Git

From the main repository folder, run:

```bash
git status
```

You should normally see:

```text
app/streamlit_app.py
reflections/phase-08-reflection.md
```

If you added or cleaned sample rows, you may also see:

```text
app/data/results.csv
```

Review the app change:

```bash
git diff app/streamlit_app.py
```

## Step 18: Commit And Push

Stage only the Phase 08 files:

```bash
git add app/streamlit_app.py reflections/phase-08-reflection.md
```

If you intentionally changed the CSV, include it:

```bash
git add app/data/results.csv
```

Commit:

```bash
git commit -m "Complete phase 08 Streamlit app"
```

Push:

```bash
git push -u origin phase-08-streamlit-app
```

## Step 19: Open A Pull Request

Open a pull request from:

```text
phase-08-streamlit-app -> main
```

Fill out the pull request template.

In the AI disclosure, include any prompt you used to understand Streamlit, localhost, widgets, metrics, charts, or error messages.

## Common Stuck Points

### `streamlit: command not found`

Try:

```bash
python3 -m streamlit run streamlit_app.py
```

If that works, Streamlit is installed but the shell command is not directly available.

### `ModuleNotFoundError: No module named 'streamlit'`

Install requirements from the repository root:

```bash
python3 -m pip install -r requirements.txt
```

### Browser does not open

Look at Terminal for a URL such as:

```text
http://localhost:8501
```

Open that URL manually.

### The app keeps rerunning

That is normal. Streamlit reruns the script when widgets change.

### File path errors

Run Streamlit from inside the `app` folder:

```bash
cd app
streamlit run streamlit_app.py
```

The app expects:

```python
DATA_FILE = "data/results.csv"
```

### Chart looks backwards

For timed events, lower is better. Improvement may appear as the line moving downward.

## AI Guidelines For This Phase

Good AI prompts:

```text
I am in Phase 08. Explain what st.selectbox does using my event filter.
```

```text
I got a Streamlit localhost issue. Explain the clue, but do not rewrite my whole app.
```

```text
Ask me questions to check whether I understand the difference between a terminal app and a Streamlit app.
```

Avoid prompts like:

```text
Write the complete Phase 08 Streamlit app for me.
```

## Demo

Show:

- `app/streamlit_app.py` in VS Code.
- The Streamlit app running in Terminal.
- The browser app at localhost.
- Results table.
- Event filter.
- Metrics.
- Goal progress.
- Simple chart.
- Your Phase 08 reflection.

Explain:

- What Streamlit is.
- What localhost means.
- How the browser app differs from `python3 app.py`.
- What widget you used.
- What pandas calculation powers one metric.
- What the chart shows.
- One error or mistake you saw.
- How AI helped, if you used it.

Live change:

- Change one title, label, or metric display without AI.
- Save the file.
- Watch Streamlit rerun.
- Explain why the browser updated.

## Good Enough To Move On

You are ready for Phase 09 when:

- You can run the Streamlit app locally.
- You can explain localhost.
- You can display CSV results in the browser.
- You can filter one event.
- You can show at least one metric and one chart.
- You can make one small UI change without AI.
- You committed and pushed your Phase 08 work.
- You opened a pull request and completed the AI disclosure.
