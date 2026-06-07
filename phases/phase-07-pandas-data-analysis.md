# Phase 07: pandas Data Analysis

## Goal

Use pandas to analyze saved track results from a CSV file.

By the end of this phase, you should be able to load `results.csv` into a pandas DataFrame, inspect rows and columns, convert the mark column to numbers, calculate basic statistics, filter results, sort results, and explain one useful insight from the data.

## Why This Phase Matters

Phase 06 taught the app how to remember results in a CSV file.

Phase 07 turns those saved results into analysis. This is where Python starts feeling like a data tool, not just a terminal input program.

pandas is widely used for data analysis in Python. It can feel powerful and unfamiliar at first, so this phase focuses on a small number of useful operations.

## Time Estimate

Plan for 2-3 hours.

The ideas are manageable, but pandas has new vocabulary. Read slowly and run the code after each step.

## Before You Start

You should be able to:

- Run `python3 app.py`.
- Explain CSV persistence.
- Open and read `app/data/results.csv`.
- Explain rows and columns at a basic level.
- Explain lists and functions.
- Commit, push, and open a pull request.

## New Concepts

### pandas

pandas is a Python library for working with table-like data.

Import it like this:

```python
import pandas as pd
```

The nickname `pd` is a common convention.

### DataFrame

A DataFrame is a table inside Python.

Excel analogy:

- A DataFrame is like a spreadsheet.
- Columns have names.
- Rows hold records.
- Each cell has one value.

### Series

A Series is one column from a DataFrame.

Example:

```python
df["mark"]
```

### Numeric Column

CSV files store text. pandas can convert a text column into numbers:

```python
df["mark"] = pd.to_numeric(df["mark"])
```

### Filtering

Filtering means keeping only rows that match a condition.

Example:

```python
df[df["event"] == "400m"]
```

### Sorting

Sorting changes the order of rows.

Example:

```python
df.sort_values("mark")
```

For timed running events, lower marks are better, so sorting ascending puts best results first.

## Step 1: Start From `main`

Make sure your local `main` branch is up to date:

```bash
git switch main
git pull
```

Create your Phase 07 branch:

```bash
git switch -c phase-07-pandas-analysis
```

If the branch already exists, use:

```bash
git switch phase-07-pandas-analysis
```

Check:

```bash
git status
```

Expected idea: Git should say you are on branch `phase-07-pandas-analysis`.

## Step 2: Confirm pandas Is Available

From the repository root, run:

```bash
python3 -m pip show pandas
```

If pandas is not installed, install requirements:

```bash
python3 -m pip install -r requirements.txt
```

Then check again:

```bash
python3 -m pip show pandas
```

## Step 3: Inspect The CSV File

Open:

```text
app/data/results.csv
```

Make sure it has a header row:

```csv
date,event,mark,meet,notes
```

For this phase, the file should have at least three data rows. If it does not, add simple sample rows:

```csv
2026-04-12,400m,58.20,Spring Invite,Sample result
2026-04-19,400m,57.85,County Championship,Sample result
2026-05-03,800m,132.40,Regional Qualifier,Sample result
```

Keep the sample data public-safe.

## Step 4: Import pandas

Open:

```text
app/app.py
```

Near the top, add:

```python
import pandas as pd
```

Keep the CSV path:

```python
DATA_FILE = "data/results.csv"
```

## Step 5: Load The CSV Into A DataFrame

Add a function:

```python
def load_results_dataframe():
    return pd.read_csv(DATA_FILE)
```

Call it near the bottom:

```python
df = load_results_dataframe()
print(df)
```

Run the app:

```bash
cd app
python3 app.py
cd ..
```

Expected idea: the CSV should print as a table.

## Step 6: Inspect The DataFrame

Try these one at a time:

```python
print(df.head())
```

`head()` shows the first few rows.

```python
print(df.columns)
```

`columns` shows the column names.

```python
print(df.shape)
```

`shape` shows row count and column count.

Run the app after each change.

## Step 7: Convert Marks To Numbers

Add this after loading the DataFrame:

```python
df["mark"] = pd.to_numeric(df["mark"])
```

This tells pandas to treat `mark` as a number instead of text.

If this fails, check `results.csv` for values like:

```text
57.85 seconds
```

For this phase, marks should be plain numbers:

```text
57.85
```

## Step 8: Count Results By Event

Add:

```python
results_by_event = df["event"].value_counts()
print(results_by_event)
```

Expected idea: pandas should show how many rows each event has.

Example:

```text
400m    2
800m    1
```

## Step 9: Find Best Result By Event

For timed events, lower is better.

Add:

```python
best_by_event = df.groupby("event")["mark"].min()
print(best_by_event)
```

Explain out loud:

- What column is being grouped?
- What column is being analyzed?
- Why does `min()` mean best for timed events?

## Step 10: Find Average Result By Event

Add:

```python
average_by_event = df.groupby("event")["mark"].mean()
print(average_by_event)
```

The average gives a general sense of performance for each event.

It is not always the most important stat, but it is a useful pandas practice.

## Step 11: Sort Results

Add:

```python
sorted_results = df.sort_values("mark")
print(sorted_results)
```

For timed events, the fastest marks should appear first.

Important beginner note: this mixes events. A 400m time and an 800m time are not directly comparable. Sorting is still useful for practicing pandas.

## Step 12: Filter One Event

Add:

```python
event_name = input("Event to analyze: ")
event_results = df[df["event"] == event_name]
print(event_results)
```

Run the app and enter:

```text
400m
```

If nothing prints except headers, check spelling and capitalization in the CSV.

## Step 13: Analyze One Event

After filtering, add:

```python
if len(event_results) == 0:
    print("No results found for that event.")
else:
    best_result = event_results["mark"].min()
    average_result = event_results["mark"].mean()
    number_of_results = len(event_results)

    print(f"Best {event_name}: {best_result}")
    print(f"Average {event_name}: {average_result}")
    print(f"Number of {event_name} results: {number_of_results}")
```

This combines pandas with conditionals from Phase 03.

## Step 14: Create A Clean Analysis Function

Move the one-event analysis into a function:

```python
def analyze_event(df, event_name):
    event_results = df[df["event"] == event_name]

    if len(event_results) == 0:
        print("No results found for that event.")
    else:
        best_result = event_results["mark"].min()
        average_result = event_results["mark"].mean()
        number_of_results = len(event_results)

        print(f"Best {event_name}: {best_result}")
        print(f"Average {event_name}: {average_result}")
        print(f"Number of {event_name} results: {number_of_results}")
```

Call it:

```python
event_name = input("Event to analyze: ")
analyze_event(df, event_name)
```

## Step 15: Keep The Main Flow Simple

The bottom of the file might look something like:

```python
show_welcome()

df = load_results_dataframe()
df["mark"] = pd.to_numeric(df["mark"])

print(df.head())

event_name = input("Event to analyze: ")
analyze_event(df, event_name)
```

It is okay if your final Phase 07 app is analysis-focused. Phase 08 will turn the project into a Streamlit app.

## Step 16: Practice A pandas Mistake

This step is optional but useful.

Temporarily misspell a column:

```python
df["marks"]
```

Run the app.

pandas should show a `KeyError`.

Read the error, then fix the column name:

```python
df["mark"]
```

Do not commit broken code.

## Step 17: Create Your Phase Reflection

Create:

```text
reflections/phase-07-reflection.md
```

Use the template from:

```text
reflections/phase-reflection-template.md
```

Fill in short answers for:

- What pandas is
- What a DataFrame is
- What rows and columns are
- Why `mark` needs to become numeric
- One statistic you calculated
- One insight from the data
- Whether you used AI

## Step 18: Check Your Work With Git

From the main repository folder, run:

```bash
git status
```

You should normally see:

```text
app/app.py
app/data/results.csv
reflections/phase-07-reflection.md
```

Review the code change:

```bash
git diff app/app.py
```

Review data changes:

```bash
git diff app/data/results.csv
```

## Step 19: Commit And Push

Stage only the Phase 07 files:

```bash
git add app/app.py app/data/results.csv reflections/phase-07-reflection.md
```

Commit:

```bash
git commit -m "Complete phase 07 pandas analysis"
```

Push:

```bash
git push -u origin phase-07-pandas-analysis
```

## Step 20: Open A Pull Request

Open a pull request from:

```text
phase-07-pandas-analysis -> main
```

Fill out the pull request template.

In the AI disclosure, include any prompt you used to understand pandas, DataFrames, filtering, grouping, sorting, numeric conversion, or error messages.

## Common Stuck Points

### `ModuleNotFoundError: No module named 'pandas'`

pandas is not installed in the Python environment you are using.

From the repository root, run:

```bash
python3 -m pip install -r requirements.txt
```

### `FileNotFoundError`

Check:

- Are you running the app from inside `app`?
- Does `app/data/results.csv` exist?
- Is `DATA_FILE` set to `"data/results.csv"`?

### `KeyError`

pandas cannot find a column with that name.

Check spelling against:

```python
print(df.columns)
```

### Numeric conversion fails

The `mark` column probably contains text that is not a plain number.

Use:

```text
57.85
```

Not:

```text
57.85 seconds
```

### Sorting mixes events

That is okay for practice, but be careful interpreting it.

A 400m time and 800m time should not be compared as if they are the same event.

## AI Guidelines For This Phase

Good AI prompts:

```text
I am in Phase 07. Explain this pandas line like I am new to DataFrames: df.groupby(\"event\")[\"mark\"].min()
```

```text
I got a KeyError in pandas. Explain the clue, but do not rewrite my whole program.
```

```text
Ask me questions to check whether I understand DataFrames, columns, and filtering.
```

Avoid prompts like:

```text
Write the complete Phase 07 pandas analysis program for me.
```

## Demo

Show:

- `app/data/results.csv`.
- `app/app.py` in VS Code.
- The app running in Terminal.
- The DataFrame or first rows printed.
- One event filtered.
- One statistic, such as best result by event.
- Your Phase 07 reflection.

Explain:

- What pandas is.
- What a DataFrame is.
- What rows and columns are.
- Why `mark` needs numeric conversion.
- What filtering does.
- What one statistic means.
- One error or mistake you saw.
- How AI helped, if you used it.

Live change:

- Add one row to `app/data/results.csv`.
- Run the app again.
- Explain how the statistic changed.

## Good Enough To Move On

You are ready for Phase 08 when:

- You can load `results.csv` with pandas.
- You can explain a DataFrame using a spreadsheet analogy.
- You can filter one event.
- You can calculate at least one statistic.
- You can explain one insight from the data.
- You can add one CSV row and rerun the analysis without AI.
- You committed and pushed your Phase 07 work.
- You opened a pull request and completed the AI disclosure.

