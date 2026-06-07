# Phase 10: Final Demo and Retrospective

## Goal

Complete the bootcamp with a final project demo and a thoughtful retrospective.

By the end of this phase, you should be able to run the final app, explain the most important files, describe the major concepts from the bootcamp, make one small live change without AI, and reflect on what you learned.

## Why This Phase Matters

A project is not really finished until you can explain it.

The final demo proves that the student understands the work, not just that the files exist. The retrospective helps turn a set of coding tasks into a clear learning story.

## Time Estimate

Plan for 2-3 hours.

This phase is mostly review, explanation, cleanup, and demo practice.

## Before You Start

You should be able to:

- Run the terminal app.
- Run the Streamlit app.
- Explain where data is stored.
- Explain the GitHub workflow.
- Explain how AI was used.
- Open a pull request.

## Final Deliverables

Create or update:

```text
README.md
app/README.md
reflections/final-retrospective.md
docs/final-demo-checklist.md
```

If needed, you may also update:

```text
app/streamlit_app.py
app/data/results.csv
```

Keep final changes small. This phase is about explaining and polishing, not rebuilding the app.

## Step 1: Start From `main`

Make sure your local `main` branch is up to date:

```bash
git switch main
git pull
```

Create your Phase 10 branch:

```bash
git switch -c phase-10-final-demo-retrospective
```

If the branch already exists, use:

```bash
git switch phase-10-final-demo-retrospective
```

Check:

```bash
git status
```

Expected idea: Git should say you are on branch `phase-10-final-demo-retrospective`.

## Step 2: Run The App

Run the terminal app:

```bash
cd app
python3 app.py
cd ..
```

Run the Streamlit app:

```bash
cd app
streamlit run streamlit_app.py
cd ..
```

If `streamlit` does not work, use:

```bash
cd app
python3 -m streamlit run streamlit_app.py
cd ..
```

Confirm:

- The app starts.
- The data file exists.
- The Streamlit app opens in a browser.
- The table, metrics, and chart work if they were completed in Phase 08.

## Step 3: Review The Important Files

Open these files and explain what each one does:

```text
README.md
AI_GUIDELINES.md
CONCEPTS.md
app/README.md
app/app.py
app/streamlit_app.py
app/data/results.csv
requirements.txt
```

You do not need to explain every file in the repository. Focus on the app and the learning materials.

## Step 4: Create The Final Demo Checklist

Create:

```text
docs/final-demo-checklist.md
```

Add:

```markdown
# Final Demo Checklist

- [ ] I can run the terminal app.
- [ ] I can run the Streamlit app.
- [ ] I can explain what the app does.
- [ ] I can explain where the data lives.
- [ ] I can explain one Python concept.
- [ ] I can explain one pandas concept.
- [ ] I can explain one Streamlit concept.
- [ ] I can explain one Git or GitHub concept.
- [ ] I can explain how I used AI.
- [ ] I can make one small live change without AI.
- [ ] I can explain what I would build next.
```

Use this during demo practice.

## Step 5: Create The Final Retrospective

Create:

```text
reflections/final-retrospective.md
```

Use this structure:

```markdown
# Final Retrospective

## What I Built


## What I Learned About Python


## What I Learned About Git And GitHub


## What I Learned About Data


## What I Learned About Streamlit


## How I Used AI


## A Bug Or Mistake I Worked Through


## What I Am Proud Of


## What I Would Build Next


## Advice For A Future Beginner

```

Write in your own words. Short, honest answers are better than polished answers you cannot explain.

## Step 6: Polish The Root README

Open:

```text
README.md
```

Check whether it clearly answers:

- What is this repository?
- What is Track Career Analyzer?
- Who is this for?
- Where are the phase guides?
- How can someone run the app?
- What is the license?

Add a short final status note:

```markdown
## Bootcamp Status

Core curriculum phases 00-10 are drafted.
```

If the app is deployed, include the app link. If not, keep the local run instructions clear.

## Step 7: Polish The App README

Open:

```text
app/README.md
```

Confirm it explains:

- How to run `app.py`
- How to run `streamlit_app.py`
- Where data lives
- Whether the app is deployed

Keep this practical. A beginner should be able to follow it.

## Step 8: Practice The Demo Script

Use this script:

```text
1. This is Track Career Analyzer.
2. It started as a small Python terminal app.
3. It grew into a CSV-backed data analysis app.
4. It uses pandas to analyze results.
5. It uses Streamlit to show results in a browser.
6. The data lives in app/data/results.csv.
7. Git tracked the work locally.
8. GitHub stored the work remotely and supported pull requests.
9. AI helped as a tutor, debugger, and reviewer.
10. I can explain the code I changed.
```

Do not memorize it word-for-word. Use it as a guide.

## Step 9: Make One Small Live Change

Choose one simple live change for the demo:

- Change a Streamlit title.
- Change a label.
- Add one row to the CSV.
- Change a printed message.
- Add one sentence to the README.

During the demo:

1. Make the change without AI.
2. Save the file.
3. Run the app or show the changed file.
4. Explain what changed.

## Step 10: Explain AI Use

Be specific.

Good explanation:

```text
I used AI to explain error messages and ask me review questions. I did not use it to submit code I could not explain.
```

Avoid vague explanation:

```text
AI helped with stuff.
```

The goal is responsible AI use.

## Step 11: Check Your Work With Git

From the main repository folder, run:

```bash
git status
```

You should normally see:

```text
README.md
app/README.md
docs/final-demo-checklist.md
reflections/final-retrospective.md
```

Review README changes:

```bash
git diff README.md app/README.md
```

## Step 12: Commit And Push

Stage only the Phase 10 files:

```bash
git add README.md app/README.md docs/final-demo-checklist.md reflections/final-retrospective.md
```

If you intentionally changed app/data files, add those too:

```bash
git add app/streamlit_app.py app/data/results.csv app/app.py
```

Commit:

```bash
git commit -m "Complete phase 10 final demo retrospective"
```

Push:

```bash
git push -u origin phase-10-final-demo-retrospective
```

## Step 13: Open A Pull Request

Open a pull request from:

```text
phase-10-final-demo-retrospective -> main
```

Fill out the pull request template.

In the AI disclosure, include any prompt you used to prepare the demo, review the README, or reflect on the project.

## Common Stuck Points

### The demo feels too long

Keep it focused.

Show the app, explain the main files, explain one concept, make one live change, and reflect.

### The student wants to keep adding features

Make a list of future ideas, but do not rebuild the app during Phase 10.

### The student cannot explain a section

Slow down and review it. The goal is understanding, not speed.

### AI wrote too much of the explanation

Rewrite the explanation in the student's own words.

## AI Guidelines For This Phase

Good AI prompts:

```text
I am preparing my final demo. Ask me questions to check whether I understand my project.
```

```text
Review my final retrospective for clarity, but do not rewrite it in a more advanced voice.
```

```text
Help me explain this error I fixed in beginner-friendly language.
```

Avoid prompts like:

```text
Write my final retrospective so it sounds impressive.
```

## Demo

Show:

- Final app running locally or deployed.
- Important files.
- Data file.
- Final demo checklist.
- Final retrospective.
- GitHub pull request history.

Explain:

- What the app does.
- What Python does.
- What Git does.
- What GitHub does.
- What pandas does.
- What Streamlit does.
- How AI helped.
- What bug or mistake you worked through.
- What you would build next.

Live change:

- Make one small change without AI.
- Run or show the result.
- Explain the change.

## Good Enough To Complete The Bootcamp

The bootcamp is complete when:

- The app can be demonstrated.
- The student can explain the main files.
- The student can explain the major tools.
- The student can describe how data moves through the app.
- The student can explain how AI was used responsibly.
- The student can make one small live change without AI.
- The final retrospective is complete.
- The final pull request is opened and reviewed.

