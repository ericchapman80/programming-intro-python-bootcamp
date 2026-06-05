# Programming Intro Python Bootcamp

A beginner-friendly software engineering bootcamp for an incoming college freshman preparing for an introductory Python course.

This is a curriculum repository. The project app built through the phases is **Track Career Analyzer**, a Python project that grows from a terminal program into a simple data analysis and Streamlit app.

## Goals

- Learn how local development works on a MacBook.
- Learn Python fundamentals through a real project.
- Practice using Terminal, VS Code, Git, GitHub, Markdown, CSV files, pandas, and Streamlit.
- Build work in small phases, using branches and pull requests.
- Use AI as a tutor and reviewer without letting it replace student understanding.
- Finish with a demo-ready app and a clear explanation of how it works.

## Who This Is For

The first student is Riley Chapman, an incoming college freshman and track and field athlete considering Computer Science. The curriculum should remain reusable for future beginner programming students.

The course assumes:

- No prior programming experience required
- macOS
- VS Code
- Terminal
- GitHub account
- Willingness to explain code out loud

## Bootcamp Roadmap

The bootcamp is designed for 10 phases, roughly 3-5 hours per week and 25-40 total hours.

| Phase | Focus | Main Deliverable |
| --- | --- | --- |
| 00 | Developer workstation | Tools verified and Phase 00 reflection PR |
| 01 | First Python program | `app/app.py` update and Phase 01 reflection PR |
| 02 | Variables and input | Athlete profile terminal program |
| 03 | Conditionals | Goal comparison logic |
| 04 | Lists and loops | Multiple results and best result |
| 05 | Functions | Cleaner reusable code |
| 06 | CSV files | Saved results in `app/data/results.csv` |
| 07 | pandas | Data analysis summaries |
| 08 | Streamlit | Phone-friendly web app |
| 09 | Deployment | Public-readiness and sharing |
| 10 | Final demo | Walkthrough and retrospective |

## Repository Layout

```text
.
├── AI_GUIDELINES.md
├── CONCEPTS.md
├── README.md
├── app/
├── cheatsheets/
├── docs/
├── instructor/
├── phases/
└── reflections/
```

## Start Here

This README is the map for the bootcamp. The first real work happens in [Phase 00: Developer Workstation](phases/phase-00-developer-workstation.md).

If you are the student, start there and follow the instructions one step at a time. Phase 00 teaches how to open Terminal, find the project folder, verify tools, and open the repo in VS Code.

If you are the reviewer or instructor, read these first:

- [AI Guidelines](AI_GUIDELINES.md)
- [Reviewer Guide](docs/reviewer-guide.md)
- [Demo Guide](docs/demo-guide.md)

## GitHub Workflow

Each phase should use this workflow:

1. Create a branch, such as `phase-01-first-python`.
2. Complete the phase work.
3. Run the code.
4. Commit changes.
5. Push the branch.
6. Open a pull request.
7. Complete the PR template, including AI usage disclosure.
8. Demo the work.
9. Address review feedback.
10. Merge.

## Public Repo Notes

Before publishing publicly:

- Confirm there is no private student information beyond what you intentionally want public.
- Confirm the MIT license is the intended reuse policy.
- Confirm sample data is safe to publish.
- Confirm instructor materials do not contain full answer keys.
- Review `.gitignore` before committing generated files.

## License

This project is available under the [MIT License](LICENSE).

## Key Documents

- [AI Guidelines](AI_GUIDELINES.md)
- [Concept Glossary](CONCEPTS.md)
- [Project Roadmap](docs/project-roadmap.md)
- [Repo Strategy](docs/repo-strategy.md)
- [Reviewer Guide](docs/reviewer-guide.md)
- [Terminal Cheat Sheet](cheatsheets/terminal-cheat-sheet.md)
- [Git Cheat Sheet](cheatsheets/git-cheat-sheet.md)
