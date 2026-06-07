# Phase 06: CSV Files and Persistence

## Goal

Save track results in a CSV file so data does not disappear when the program ends.

By the end of this phase, you should be able to explain what persistence means, read rows from a CSV file, append a new result, save it, and display the saved results when the app runs again.

## Why This Phase Matters

So far, the app forgets everything when it stops running.

That is normal for beginner programs, but real apps usually need to remember data. Phase 06 introduces persistence: storing information outside the running program.

CSV files are a good first storage format because they are plain text and can also be opened like a spreadsheet.

## Time Estimate

Plan for 2-3 hours.

File paths and CSV reading can be picky. Move slowly and test after each small change.

## Before You Start

You should be able to:

- Run `python3 app.py`.
- Explain functions.
- Explain lists and loops.
- Explain `append()`.
- Explain what a file path is.
- Commit, push, and open a pull request.

## New Concepts

### Persistence

Persistence means data is saved somewhere after the program ends.

Example:

```text
app/data/results.csv
```

If results are saved in that file, the next app run can load them again.

### CSV

CSV means comma-separated values.

Example:

```csv
date,event,mark,meet,notes
2026-04-12,400m,58.20,Spring Invite,Sample result
```

Each line is a row. Each comma separates columns.

### Header Row

The first row usually names the columns.

Example:

```csv
date,event,mark,meet,notes
```

### File Path

A file path tells Python where a file lives.

Example:

```python
DATA_FILE = "data/results.csv"
```

If you run Python from inside the `app` folder, that path points to:

```text
app/data/results.csv
```

### `csv` Module

Python includes a built-in `csv` module for working with CSV files.

Example:

```python
import csv
```

No install is needed.

### Dictionary Row

This phase uses `csv.DictReader` and `csv.DictWriter`.

That lets each CSV row behave like a dictionary:

```python
row["event"]
row["mark"]
```

Do not worry if dictionaries are new. In this phase, think of a dictionary row as a labeled row from the CSV.

## Step 1: Start From `main`

Make sure your local `main` branch is up to date:

```bash
git switch main
git pull
```

Create your Phase 06 branch:

```bash
git switch -c phase-06-csv-persistence
```

If the branch already exists, use:

```bash
git switch phase-06-csv-persistence
```

Check:

```bash
git status
```

Expected idea: Git should say you are on branch `phase-06-csv-persistence`.

## Step 2: Look At The Sample CSV

Open:

```text
app/data/sample_results.csv
```

Read the header row:

```csv
date,event,mark,meet,notes
```

Each future result should use the same kind of columns.

## Step 3: Create The Working Results File

Create a new file:

```text
app/data/results.csv
```

Start it with only the header row:

```csv
date,event,mark,meet,notes
```

This file will become the student's working data file.

## Step 4: Import The CSV Module

Open:

```text
app/app.py
```

At the top of the file, add:

```python
import csv
```

Then define the data file path:

```python
DATA_FILE = "data/results.csv"
```

Use uppercase for `DATA_FILE` because it is a constant: a value the program expects to keep using.

## Step 5: Write A Function To Load Results

Add:

```python
def load_results():
    results = []

    with open(DATA_FILE, "r", newline="") as file:
        reader = csv.DictReader(file)

        for row in reader:
            results.append(row)

    return results
```

This function:

- Opens the CSV file.
- Reads each row.
- Adds each row to a list.
- Returns the list.

Run the app after adding the function. It may not display anything new yet.

## Step 6: Display Saved Results

Add a function:

```python
def display_saved_results(results):
    print()
    print("Saved Results")
    print("-------------")

    if len(results) == 0:
        print("No saved results yet.")
    else:
        for result in results:
            print(f"{result['date']} | {result['event']} | {result['mark']} | {result['meet']}")
```

Call it near the bottom of the file:

```python
saved_results = load_results()
display_saved_results(saved_results)
```

Run the app:

```bash
cd app
python3 app.py
cd ..
```

Expected idea: if `results.csv` only has the header row, the app should say:

```text
No saved results yet.
```

## Step 7: Write A Function To Add One Result

Add:

```python
def add_result():
    date = input("Date (YYYY-MM-DD): ")
    event = input("Event: ")
    mark = input("Mark: ")
    meet = input("Meet: ")
    notes = input("Notes: ")

    return {
        "date": date,
        "event": event,
        "mark": mark,
        "meet": meet,
        "notes": notes,
    }
```

For this phase, store `mark` as text in the CSV. Pandas will help with numeric analysis in Phase 07.

## Step 8: Write A Function To Save One Result

Add:

```python
def save_result(result):
    fieldnames = ["date", "event", "mark", "meet", "notes"]

    with open(DATA_FILE, "a", newline="") as file:
        writer = csv.DictWriter(file, fieldnames=fieldnames)
        writer.writerow(result)
```

The `"a"` means append. It adds to the end of the file instead of replacing the whole file.

## Step 9: Connect Add And Save

Near the bottom of the file, add:

```python
new_result = add_result()
save_result(new_result)
```

Run the app and enter a result.

Then open:

```text
app/data/results.csv
```

You should see a new row.

## Step 10: Load Again After Saving

After saving, load and display the results again:

```python
new_result = add_result()
save_result(new_result)

saved_results = load_results()
display_saved_results(saved_results)
```

Run the app twice.

Expected idea: results from the first run should still be there during the second run.

That is persistence.

## Step 11: Keep The Main Flow Readable

The bottom of the file might look something like this:

```python
show_welcome()

saved_results = load_results()
display_saved_results(saved_results)

new_result = add_result()
save_result(new_result)

saved_results = load_results()
display_saved_results(saved_results)
```

This is enough for Phase 06.

Do not build a full menu yet unless your reviewer asks for it. Menus can distract from the main goal: reading and writing CSV files.

## Step 12: Practice A File Path Mistake

This step is optional but useful.

Temporarily change:

```python
DATA_FILE = "data/results.csv"
```

To:

```python
DATA_FILE = "results.csv"
```

Run the app from inside `app`.

Python may not find the expected file or may write a file in the wrong place.

Read the error or inspect where the file was created. Then fix the path immediately:

```python
DATA_FILE = "data/results.csv"
```

Do not commit the wrong path.

## Step 13: Create Your Phase Reflection

Create:

```text
reflections/phase-06-reflection.md
```

Use the template from:

```text
reflections/phase-reflection-template.md
```

Fill in short answers for:

- What persistence means
- What a CSV file is
- What the header row does
- What `load_results()` does
- What `save_result()` does
- One file path mistake or CSV mistake you saw
- Whether you used AI

## Step 14: Check Your Work With Git

From the main repository folder, run:

```bash
git status
```

You should normally see:

```text
app/app.py
app/data/results.csv
reflections/phase-06-reflection.md
```

Review the code change:

```bash
git diff app/app.py
```

Review the CSV change:

```bash
git diff app/data/results.csv
```

## Step 15: Commit And Push

Stage only the Phase 06 files:

```bash
git add app/app.py app/data/results.csv reflections/phase-06-reflection.md
```

Commit:

```bash
git commit -m "Complete phase 06 CSV persistence"
```

Push:

```bash
git push -u origin phase-06-csv-persistence
```

## Step 16: Open A Pull Request

Open a pull request from:

```text
phase-06-csv-persistence -> main
```

Fill out the pull request template.

In the AI disclosure, include any prompt you used to understand CSV files, file paths, `with open`, `DictReader`, `DictWriter`, or error messages.

## Common Stuck Points

### `FileNotFoundError`

Python cannot find the file path.

Check:

- Are you running the app from inside `app`?
- Does `app/data/results.csv` exist?
- Is `DATA_FILE` set to `"data/results.csv"`?

### CSV row is written on the same line

Make sure the `open()` call includes:

```python
newline=""
```

### The header row gets duplicated

This phase starts `results.csv` with the header row manually.

The app should append rows, not write the header each time.

### The mark is text

That is okay for Phase 06.

Phase 07 introduces pandas, which can help convert columns for analysis.

### The app saves too many rows while testing

That is normal during practice.

You can manually clean `app/data/results.csv`, but keep the header row.

## AI Guidelines For This Phase

Good AI prompts:

```text
I am in Phase 06. Explain what this with open block does line by line.
```

```text
I got a FileNotFoundError. Explain the clue, but do not rewrite my whole program.
```

```text
Ask me questions to check whether I understand persistence and CSV files.
```

Avoid prompts like:

```text
Write the complete Phase 06 CSV persistence program for me.
```

## Demo

Show:

- `app/data/results.csv` before running the app.
- The app running in Terminal.
- A new result being entered.
- `app/data/results.csv` after running the app.
- The saved result displayed when the app runs again.
- Your Phase 06 reflection.

Explain:

- What persistence means.
- What CSV means.
- What the header row does.
- What `load_results()` does.
- What `save_result()` does.
- Why the file path matters.
- One error or mistake you saw.
- How AI helped, if you used it.

Live change:

- Add one new notes value or change a saved row manually.
- Run the app again.
- Explain why the app can see the changed CSV data.

## Good Enough To Move On

You are ready for Phase 07 when:

- You can save a result to `app/data/results.csv`.
- You can run the app again and see saved results.
- You can explain persistence.
- You can explain the CSV header row.
- You can explain `load_results()` and `save_result()`.
- You can make one small CSV change without AI.
- You committed and pushed your Phase 06 work.
- You opened a pull request and completed the AI disclosure.

