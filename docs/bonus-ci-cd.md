# Bonus: CI/CD With GitHub Actions

This is an optional bonus topic. It is not required for the main beginner bootcamp.

## What CI/CD Means

CI means continuous integration.

Beginner explanation: when code is pushed to GitHub or a pull request is opened, GitHub can automatically run checks.

CD means continuous delivery or continuous deployment.

Beginner explanation: after checks pass, a system may automatically prepare or publish the app.

For this bootcamp, focus on CI first.

## Why It Is Optional

CI/CD is useful, but it adds another layer of tools and vocabulary.

The main bootcamp goals are:

- Learn Python
- Learn Terminal and VS Code
- Learn Git and GitHub
- Build an app gradually
- Analyze CSV data
- Build a Streamlit app
- Explain the code clearly

CI/CD can come later as an extra professional workflow.

## Good First CI Example

A future bonus exercise could add a GitHub Actions workflow that checks:

- Python can start
- Required packages install
- Basic files exist
- Optional future tests pass

Example workflow path:

```text
.github/workflows/python-checks.yml
```

Do not add this workflow until the student has enough context to understand why it exists.

## Coaching Questions

- What should happen automatically when a pull request opens?
- What check would catch a broken Python file?
- Why is it useful for GitHub to run checks before merge?
- What is the difference between a local check and a GitHub check?
- Why might deployment automation be risky before privacy review?

## Good Enough For A Bonus Demo

The student can explain:

- What CI means
- What GitHub Actions does
- What event triggers the workflow
- What command the workflow runs
- How a failed check protects `main`

