# Phase 09 Review Checklist

Use this checklist while reviewing the student's Phase 09 pull request and demo.

## Expected Deliverables

The student should update or add:

```text
README.md
app/README.md
docs/sharing-note-template.md
reflections/phase-09-reflection.md
```

The student may also update:

```text
app/streamlit_app.py
app/data/results.csv
```

Deployment is encouraged if the app and data are ready, but it is acceptable to defer deployment with a clear explanation.

## Commands The Student Should Be Able To Run

```bash
git switch main
git pull
git switch -c phase-09-deployment-sharing
cd app
streamlit run streamlit_app.py
python3 -m streamlit run streamlit_app.py
cd ..
python3 -m pip install -r requirements.txt
git status
git diff README.md app/README.md
git add README.md app/README.md docs/sharing-note-template.md reflections/phase-09-reflection.md
git commit -m "Complete phase 09 deployment sharing"
git push -u origin phase-09-deployment-sharing
```

The student does not need to have every command memorized, but should understand the main flow.

## Questions To Ask

- What does deployment mean?
- What is the difference between localhost and a deployed URL?
- What data did you check before sharing?
- What would count as a secret?
- What file does Streamlit Community Cloud run?
- What dependencies does the app need?
- Did you deploy the app? Why or why not?
- How can someone else run or view the app?
- What changed in this pull request?
- Did you use AI? What did it help you understand?

## Common Mistakes To Watch For

- Student wants to deploy before checking privacy.
- Student cannot explain what data is public.
- README run instructions are incomplete.
- Wrong Streamlit entry point is used.
- Student forgets `requirements.txt`.
- Student commits secrets or local config files.
- Student treats deployment failure as a personal failure instead of a debugging task.

## Good Enough To Move On

Move on when the student can:

- Run the app locally.
- Explain how someone else can run or view it.
- Show that public data was reviewed.
- Confirm no secrets are committed.
- Explain deployment status.
- Show a sharing note.
- Make one README wording improvement live without AI.
- Show a Phase 09 reflection.
- Explain the pull request at a high level.

## Suggested Feedback Language

```text
You are ready for Phase 10 because the app is either deployed or intentionally ready for local sharing, and you can explain the privacy and README decisions.
```

```text
Before moving on, let's verify the app entry point and the data file path one more time.
```

```text
Deferring deployment is acceptable when you can clearly explain what still needs to be checked.
```

