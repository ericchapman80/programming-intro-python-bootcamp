# Phase 10 Review Checklist

Use this checklist while reviewing the student's final demo and retrospective.

## Expected Deliverables

The student should update or add:

```text
README.md
app/README.md
docs/final-demo-checklist.md
reflections/final-retrospective.md
```

The student may also update app or data files if a small final polish change is intentional.

## Commands The Student Should Be Able To Run

```bash
git switch main
git pull
git switch -c phase-10-final-demo-retrospective
cd app
python3 app.py
streamlit run streamlit_app.py
python3 -m streamlit run streamlit_app.py
cd ..
git status
git diff README.md app/README.md
git add README.md app/README.md docs/final-demo-checklist.md reflections/final-retrospective.md
git commit -m "Complete phase 10 final demo retrospective"
git push -u origin phase-10-final-demo-retrospective
```

The student does not need to have every command memorized, but should understand the main flow.

## Questions To Ask

- What does the app do?
- What did you build first?
- How did the app grow over time?
- Where does the data live?
- What does Python do in this project?
- What does pandas do?
- What does Streamlit do?
- What does Git do?
- What does GitHub do?
- How did you use AI responsibly?
- What bug or mistake did you work through?
- What would you build next?

## Common Mistakes To Watch For

- Student gives a polished answer they cannot explain.
- Student cannot run the app.
- Student cannot explain the difference between local and GitHub.
- Student cannot explain where data comes from.
- Student uses AI to write the retrospective in a voice that is not theirs.
- Student tries to add large new features instead of finishing the demo.

## Good Enough To Complete

Complete the bootcamp when the student can:

- Run or show the final app.
- Explain the main files.
- Explain the major tools.
- Explain how data moves from CSV to pandas to Streamlit.
- Explain one meaningful mistake or bug.
- Make one small live change without AI.
- Discuss AI use honestly.
- Share a clear final retrospective.

## Suggested Feedback Language

```text
You completed the bootcamp because you can run the app, explain the main code and tools, and describe how you learned through the project.
```

```text
Before calling this complete, let's practice explaining how one CSV row becomes part of the Streamlit display.
```

```text
Your next step could be adding one feature, improving the data, or creating a separate polished app repository.
```

