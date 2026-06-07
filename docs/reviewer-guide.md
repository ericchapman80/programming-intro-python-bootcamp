# Reviewer Guide

This guide helps a parent, reviewer, or instructor coach the student. The tone should be coaching-oriented, not grading-oriented.

## Review Pattern For Every Phase

Ask:

- What did you build?
- What file changed?
- How do you run it?
- What concept did you learn?
- What mistake or bug did you hit?
- Did you use AI?
- What did AI help you understand?
- Can you explain every line you changed?

Check:

- The code runs.
- The PR template is complete.
- AI usage is disclosed.
- The student can make a small live change without AI.
- The student can explain local vs remote Git workflow.

## Common Coaching Questions

- What do you expect this command to do?
- What folder are you in right now?
- What changed since the last commit?
- What does this error message say in plain English?
- What is the smallest thing we can test next?
- How would you explain this to a teammate?

## AI Misuse Looks Like

- Student cannot explain copied code.
- PR contains large code jumps beyond the phase.
- AI disclosure is empty or vague.
- Student asks AI for the whole solution instead of hints.
- Student avoids debugging by replacing code wholesale.

## Good Enough To Move On

Move on when:

- The deliverable works.
- The student can run it.
- The student can explain the main concept.
- The student can explain at least one mistake.
- The student can complete the GitHub workflow with light coaching.

## Phase Review Matrix

| Phase | Student Should Learn | Files Likely To Change | Commands To Run | Demo Check |
| --- | --- | --- | --- | --- |
| 00 | Tools, Terminal, local vs remote | `reflections/phase-00-reflection.md` | `brew --version`, `python3 --version`, `git --version`, `code --version`, `git status` | Explain each tool and show reflection |
| 01 | `.py`, `print()`, syntax | `app/app.py`, `reflections/phase-01-reflection.md` | `python3 app.py` | Change message live |
| 02 | Variables, input, type conversion | `app/app.py`, `reflections/phase-02-reflection.md` | `python3 app.py` | Enter profile twice |
| 03 | Conditionals, booleans | `app/app.py`, `reflections/phase-03-reflection.md` | `python3 app.py` | Faster/equal/still-chasing goal |
| 04 | Lists and loops | `app/app.py`, `reflections/phase-04-reflection.md` | `python3 app.py` | Add multiple results and change loop count |
| 05 | Functions | `app/app.py`, `reflections/phase-05-reflection.md` | `python3 app.py` | Explain one function and one return value |
| 06 | CSV persistence | `app/app.py`, `app/data/results.csv`, `reflections/phase-06-reflection.md` | `python3 app.py` | Save result and show CSV changed |
| 07 | pandas analysis | `app/app.py`, `app/data/results.csv`, `reflections/phase-07-reflection.md` | `python3 app.py` | Filter event and show one statistic |
| 08 | Streamlit app | `app/streamlit_app.py`, `reflections/phase-08-reflection.md` | `streamlit run streamlit_app.py` | Browser demo with table, metric, and chart |
| 09 | Deployment and sharing | `README.md`, `app/README.md`, `docs/sharing-note-template.md`, `reflections/phase-09-reflection.md` | `streamlit run streamlit_app.py` | Public-readiness check and sharing note |
| 10 | Final explanation | `README.md`, `app/README.md`, `docs/final-demo-checklist.md`, `reflections/final-retrospective.md` | `python3 app.py`, `streamlit run streamlit_app.py` | Final walkthrough and live change |

For detailed Phase 00 review guidance, use [Phase 00 Review Checklist](../instructor/reviewer-checklists/phase-00-review-checklist.md).

For detailed Phase 01 review guidance, use [Phase 01 Review Checklist](../instructor/reviewer-checklists/phase-01-review-checklist.md).

For detailed Phase 02 review guidance, use [Phase 02 Review Checklist](../instructor/reviewer-checklists/phase-02-review-checklist.md).

For detailed Phase 03 review guidance, use [Phase 03 Review Checklist](../instructor/reviewer-checklists/phase-03-review-checklist.md).

For detailed Phase 04 review guidance, use [Phase 04 Review Checklist](../instructor/reviewer-checklists/phase-04-review-checklist.md).

For detailed Phase 05 review guidance, use [Phase 05 Review Checklist](../instructor/reviewer-checklists/phase-05-review-checklist.md).

For detailed Phase 06 review guidance, use [Phase 06 Review Checklist](../instructor/reviewer-checklists/phase-06-review-checklist.md).

For detailed Phase 07 review guidance, use [Phase 07 Review Checklist](../instructor/reviewer-checklists/phase-07-review-checklist.md).

For detailed Phase 08 review guidance, use [Phase 08 Review Checklist](../instructor/reviewer-checklists/phase-08-review-checklist.md).

For detailed Phase 09 review guidance, use [Phase 09 Review Checklist](../instructor/reviewer-checklists/phase-09-review-checklist.md).

For detailed Phase 10 review guidance, use [Phase 10 Review Checklist](../instructor/reviewer-checklists/phase-10-review-checklist.md).
