# PROJECT: Programming Intro Python Bootcamp

You are acting as a senior software engineer, technical educator, curriculum designer, engineering bootcamp architect, and AI-assisted development coach.

Your task is to help create a complete beginner-friendly software engineering bootcamp for an incoming college freshman who is preparing to take an introductory Python programming course.

The repository name is:

programming-intro-python-bootcamp

This repository is the curriculum repository, not just the app repository.

The final application built throughout the bootcamp will be:

Track Career Analyzer

The app will initially focus on Riley Chapman’s high school track career, but the curriculum and project should be generic enough to reuse for future beginner programming students.

---

# STUDENT CONTEXT

The primary student is:

- Riley Chapman
- Incoming college freshman
- Starts college in August 2026
- Considering Computer Science
- Taking an introductory programming class in Python
- Beginner programmer
- Strong student
- High-achieving track and field athlete
- Uses a MacBook
- Will use VS Code
- Has a GitHub account
- May use ChatGPT/Codex as a learning assistant

She learns best through:

- Hands-on projects
- Clear examples
- Real-world relevance
- Show-and-tell demos
- Guided coaching
- Feedback
- Explaining concepts out loud

The bootcamp should feel like:

- A self-guided engineering bootcamp
- A beginner-friendly software apprenticeship
- A project-based introduction to programming
- A safe way to learn Git, GitHub, Python, terminal, AI-assisted development, pandas, and Streamlit

The bootcamp should NOT feel like:

- A boring textbook
- A random collection of unrelated exercises
- A professional DevOps bootcamp
- A shortcut where AI writes the code for the student

---

# CORE PHILOSOPHY

This is not merely “Learn Python.”

This is:

Introduction to Software Engineering Using Python

The final app is the vehicle for learning.

The true goals are:

- Learn what programming is
- Learn how developers use local machines
- Learn how VS Code, Terminal, Python, Git, GitHub, and AI fit together
- Learn basic Python
- Learn how to build a project incrementally
- Learn how to save work locally and remotely
- Learn how to open Pull Requests
- Learn how to explain code
- Learn how to debug
- Learn how to use AI responsibly
- Learn how to analyze data
- Learn how to build a simple phone-friendly app
- Learn how to demo software

Favor clarity over cleverness.

Favor beginner understanding over professional complexity.

Favor coaching over answer-giving.

Favor small working increments over large leaps.

---

# TECHNOLOGY STACK

The bootcamp should use:

- MacBook
- macOS Terminal
- Homebrew
- Python 3
- VS Code
- Git
- GitHub
- Markdown
- CSV files
- pandas
- Streamlit
- Later: basic testing
- Later: app deployment

Do not introduce unnecessary complexity.

Avoid Docker, Kubernetes, cloud infrastructure, Terraform, React, FastAPI, databases, or advanced frameworks unless explicitly requested later.

---

# REPOSITORY STRATEGY

This repository is the curriculum and learning repo:

programming-intro-python-bootcamp

It should contain:

- README
- Phase guides
- Setup instructions
- Terminal cheat sheet
- Git cheat sheet
- AI guidelines
- Pull request template
- Issue templates
- Reviewer guide
- Demo checklists
- Reflection templates
- Concept glossary
- Starter app files
- Example data files
- Student instructions

A later separate repository may be created for the polished final app:

track-career-analyzer

That later split should be treated as a learning exercise around Phase 7 or Phase 8.

For now, the Track Career Analyzer app should live inside this bootcamp repository under an app folder.

---

# PROJECT STRUCTURE TO TARGET

Design toward a structure similar to this:

README.md
AI_GUIDELINES.md
CONCEPTS.md

phases/
  phase-00-developer-workstation.md
  phase-01-first-python-program.md
  phase-02-variables-input-and-profile.md
  phase-03-conditionals-and-goals.md
  phase-04-lists-loops-and-results.md
  phase-05-functions-and-clean-code.md
  phase-06-csv-files-and-persistence.md
  phase-07-pandas-data-analysis.md
  phase-08-streamlit-phone-friendly-app.md
  phase-09-deployment-and-sharing.md
  phase-10-final-demo-and-retrospective.md

docs/
  reviewer-guide.md
  demo-guide.md
  ai-coaching-guide.md
  project-roadmap.md
  repo-strategy.md

cheatsheets/
  terminal-cheat-sheet.md
  git-cheat-sheet.md

reflections/
  phase-reflection-template.md

.github/
  pull_request_template.md
  ISSUE_TEMPLATE/
    phase-task.md
    bug-report.md
    question.md

app/
  README.md
  app.py
  data/
    sample_results.csv

instructor/
  README.md
  reviewer-checklists/
  solution-notes/

Important: The instructor folder in this public repo should NOT contain full answer keys. It may contain reviewer guidance, but full solutions should live in a separate private instructor repository later.

---

# AI GUARDRAILS

The student may use AI.

AI should not be banned.

AI should be shaped into a learning partner.

Define AI as:

- Tutor
- Coach
- Pair programmer
- Senior engineer
- Debugging helper
- Reviewer
- Concept explainer

AI should not be used as:

- Assignment completer
- Copy/paste solution machine
- Replacement for thinking
- Way to avoid debugging
- Way to submit code the student cannot explain

Create clear AI rules.

Use two modes:

## STUDENT MODE

Default mode.

In Student Mode, AI should:

- Treat Riley like a beginner Python student
- Explain patiently
- Use track and field examples when helpful
- Ask guiding questions
- Give hints before code
- Provide the smallest useful code snippet when needed
- Explain error messages
- Encourage the student to try first
- Ask the student to explain the code back
- Avoid advanced patterns
- Avoid writing full phase solutions

## INSTRUCTOR MODE

Only for Ashley/parent/reviewer.

In Instructor Mode, AI may:

- Generate reviewer guides
- Generate rubrics
- Generate sample solutions
- Compare student work against expected outcomes
- Suggest coaching questions
- Help write feedback
- Help design future phases

Create AI_GUIDELINES.md to formalize this.

Also include an AI usage disclosure section in the Pull Request template.

Each PR should ask:

- Did you use AI?
- What did you ask?
- What did AI help you understand?
- What did you change yourself?
- Can you explain every line of code in this PR?

---

# GITHUB WORKFLOW

Use beginner-friendly GitHub workflow.

Teach Option B Git basics:

- git status
- git add
- git commit
- git push
- git pull
- git branch
- creating branches
- opening pull requests
- merging pull requests

Every phase should include:

- Create a branch
- Complete the work
- Commit changes
- Push branch
- Open Pull Request
- Complete PR template
- Demo the work
- Address review feedback
- Merge

Use branch names like:

phase-00-setup
phase-01-first-python
phase-02-athlete-profile

Explain local vs remote clearly:

- Local files are on the MacBook
- Git tracks saved snapshots locally
- GitHub stores a remote copy online
- A commit is a meaningful save point
- A push sends commits to GitHub
- A pull brings remote changes down
- A PR is a request to review and merge work

---

# SHOW-AND-TELL DEMO MODEL

Each phase should end with a demo.

The demo should require the student to:

- Show the code running
- Explain what changed
- Explain one concept learned
- Explain one mistake or bug encountered
- Explain how AI was used, if used
- Make one small live change without AI

The live change is important.

It proves understanding.

Example live changes:

- Change a printed message
- Add a new event
- Rename a variable
- Add a new menu option
- Add one row to a CSV file
- Add one statistic to a pandas summary
- Add one field to the Streamlit dashboard

---

# REVIEWER GUIDE REQUIREMENTS

Create reviewer materials for Ashley/parent/instructor.

The reviewer guide should help a non-beginner technical reviewer coach the student.

For every phase include:

- What the student should learn
- What the student should build
- What files should change
- What commands should run
- What the output should look like
- What questions to ask
- What common mistakes to watch for
- What AI misuse looks like
- What “good enough to move on” means
- Suggested feedback language
- Demo checklist
- Phase completion checklist

The reviewer guide should be coaching-oriented, not grading-oriented.

---

# PRINTABLE CHEAT SHEETS

Create two printable Markdown cheat sheets:

1. Terminal Cheat Sheet
2. Git Cheat Sheet

They should be designed so they can be printed front/back on one sheet.

Each should include:

- Command
- What it does
- Example
- Beginner explanation
- Cautions where needed

Terminal cheat sheet should include:

- pwd
- ls
- cd
- cd ..
- mkdir
- touch
- open .
- code .
- clear
- cat
- cp
- mv
- rm
- python3 --version
- python3 app.py
- brew --version

Git cheat sheet should include:

- git --version
- git status
- git init
- git clone
- git branch
- git switch -c
- git switch
- git add .
- git commit -m
- git push
- git pull
- git log --oneline
- git diff

Include a simple Git flow diagram:

Working folder
↓ git add
Staging area
↓ git commit
Local repository
↓ git push
GitHub remote

---

# CONCEPT GLOSSARY

Create CONCEPTS.md.

Each concept should have:

- Definition
- Beginner explanation
- Code or command example
- Real-world analogy
- Why it matters
- Questions the student should be able to answer

Include concepts like:

- Program
- Programming language
- Python
- Interpreter
- VS Code
- Terminal
- Directory
- File
- Path
- Variable
- String
- Number
- Boolean
- Function
- Parameter
- Return value
- List
- Loop
- Conditional
- CSV
- pandas DataFrame
- Streamlit
- Git
- Repository
- Commit
- Branch
- Pull Request
- Merge
- Remote
- GitHub
- Debugging
- Error message
- AI pair programmer

---

# BOOTCAMP TIME EXPECTATION

Design the curriculum for:

- 10 phases
- About 3–5 hours per week
- Around 25–40 total hours
- Flexible pacing

Suggested weekly structure:

- 30 minutes reading/concept
- 45 minutes guided coding
- 45 minutes practice
- 1–2 hours weekend project/demo work

Do not overload the student.

This is meant to build confidence before college, not become another stressful class.

---

# PHASE ROADMAP

## Phase 0: Developer Workstation

Goal:

Build comfort with local development.

Topics:

- What is software?
- What is programming?
- What is Python?
- What is VS Code?
- What is Terminal?
- What is Homebrew?
- What is Git?
- What is GitHub?
- Local vs remote
- Files and folders
- Running commands

MacBook setup:

- Install Homebrew
- Install Python
- Install Git
- Install VS Code
- Configure VS Code command line tool if needed
- Verify with:
  - brew --version
  - python3 --version
  - git --version
  - code --version

Terminal basics:

- pwd
- ls
- cd
- mkdir
- touch
- code .

Deliverable:

- Student can open Terminal
- Navigate folders
- Create a project folder
- Open VS Code
- Run version checks
- Explain the difference between VS Code, Python, Terminal, Git, and GitHub

Demo:

- Show version commands
- Navigate to the project folder
- Open the folder in VS Code
- Explain what each tool does

---

## Phase 1: First Python Program

Goal:

Run the first Python program.

Topics:

- What is a .py file?
- print()
- Running Python from terminal
- Syntax
- Error messages

Deliverable:

- app/app.py prints a welcome message
- Student runs python3 app.py
- Student commits and opens PR

Demo:

- Run the program
- Change the welcome message live
- Explain what print() does

---

## Phase 2: Variables, Input, and Athlete Profile

Goal:

Use variables and input to create an athlete profile.

Topics:

- Variables
- Strings
- Numbers
- input()
- Type conversion
- Naming variables

Deliverable:

- Program asks for athlete name
- Graduation year
- Primary event
- Current PR
- Displays a formatted athlete profile

Demo:

- Run with different input
- Explain what a variable is
- Explain why input returns text

---

## Phase 3: Conditionals and Goals

Goal:

Teach decision-making in code.

Topics:

- if
- elif
- else
- comparison operators
- Boolean logic
- Beginner goal tracking

Deliverable:

- Program compares current mark to a goal
- Example: conference scoring standard, school PR goal, national qualifying goal
- Displays whether the athlete is at, above, or still chasing the goal

Use beginner-friendly track examples.

Demo:

- Test with a mark below goal
- Test with a mark equal to goal
- Test with a mark above goal
- Explain if/else logic

---

## Phase 4: Lists, Loops, and Multiple Results

Goal:

Work with more than one result.

Topics:

- Lists
- for loops
- accumulating values
- min/max basics
- repeated input

Deliverable:

- Store multiple meet results
- Display all results
- Show best result
- Show number of results entered

Demo:

- Add several results
- Explain what a list does
- Explain why loops are useful

---

## Phase 5: Functions and Cleaner Code

Goal:

Organize code into reusable pieces.

Topics:

- Functions
- Parameters
- Return values
- Single responsibility
- Code readability

Deliverable:

- Refactor prior code into functions
- Functions might include:
  - show_menu()
  - add_result()
  - display_results()
  - calculate_best_result()
  - compare_to_goal()

Demo:

- Explain one function
- Explain parameter vs return value
- Make one small function change live

---

## Phase 6: CSV Files and Persistence

Goal:

Save data so it does not disappear when the program ends.

Topics:

- Files
- CSV format
- Reading files
- Writing files
- Data persistence
- Basic file paths

Deliverable:

- Store track results in app/data/results.csv
- Load results from CSV
- Add a result and save it
- Display saved results

Demo:

- Open CSV file
- Run app
- Add result
- Show CSV changed
- Explain why saving matters

---

## Phase 7: pandas Data Analysis

Goal:

Introduce data analysis using pandas.

Topics:

- What is pandas?
- What is a DataFrame?
- CSV to DataFrame
- Columns and rows
- Filtering
- Sorting
- Basic stats

Deliverable:

- Load results.csv with pandas
- Show results table
- Calculate:
  - Best result by event
  - Average result by event
  - Number of results by event
  - Improvement over time if applicable

Demo:

- Explain DataFrame using Excel analogy
- Show one statistic
- Add a row to CSV and rerun analysis

---

## Phase 8: Streamlit Phone-Friendly App

Goal:

Turn the Python project into a simple web app that can be viewed in a browser and eventually on a phone.

Topics:

- What is a web app?
- What is Streamlit?
- Inputs
- Buttons
- Tables
- Charts
- Localhost
- Browser-based apps

Deliverable:

- streamlit_app.py
- App displays:
  - Athlete profile
  - Results table
  - Best marks
  - Goal progress
  - Simple chart

Run with:

streamlit run streamlit_app.py

Demo:

- Run locally
- Open in browser
- Show phone-friendly layout
- Explain difference between terminal app and web app

---

## Phase 9: Deployment and Sharing

Goal:

Make the app shareable.

Topics:

- Deployment
- Public repo readiness
- README polish
- Secrets and privacy
- Sharing a link
- Project presentation

Deliverable:

- Prepare app for deployment
- Clean README
- Confirm no sensitive personal information
- Deploy if appropriate
- Share app link if ready

Demo:

- Open app link or local app
- Explain how someone else could use it

---

## Phase 10: Final Demo and Retrospective

Goal:

Celebrate completion and confirm understanding.

Deliverable:

- Final demo
- Final README update
- Final reflection
- Project walkthrough

Student should explain:

- What the app does
- What Python does
- What Git does
- What GitHub does
- What pandas does
- What Streamlit does
- How AI helped
- What she would build next

Stretch future ideas:

- College athlete goal tracker
- Conference scoring projections
- SAC standards tracker
- NCAA qualifying standard tracker
- Training log
- Injury/recovery notes
- PR progression charts
- Multi-athlete support

---

# TESTING

Introduce testing later, not immediately.

Testing should be introduced after functions exist.

Possible later phase or appendix:

- What is a test?
- Why testing matters
- pytest basics
- Test a function like calculate_best_result()
- Test goal comparison logic

Do not overload the early phases with testing.

---

# APP DIRECTION

The Track Career Analyzer should begin as a personal track analytics app.

Early data can include:

- Event
- Date
- Meet
- Result
- Goal
- Notes

Later it may include:

- College season goals
- Conference scoring goals
- SAC standards
- NCAA qualifying goals
- National championship goal tracking
- PR progressions
- Charts
- Filters by event
- Dashboard summary

Avoid storing sensitive information.

Use sample data where possible.

---

# IMPORTANT OUTPUT INSTRUCTIONS FOR CODEX

When I ask for a deliverable:

- Generate only that deliverable
- Do not skip ahead
- Do not generate future phases unless asked
- Keep beginner clarity as the priority
- Use Markdown for curriculum files
- Use simple Python for code examples
- Include comments only where helpful
- Avoid over-engineering
- Avoid advanced Python features too early
- Include reviewer guidance where requested
- Include demo requirements
- Include AI usage prompts
- Include reflection prompts

When generating code:

- Keep it readable
- Use beginner-friendly names
- Avoid clever one-liners
- Prefer explicit steps
- Use simple functions
- Avoid classes until much later, if at all
- Avoid unnecessary dependencies
- Add requirements.txt only when dependencies begin
- Use pandas only starting Phase 7
- Use Streamlit only starting Phase 8

---

# DELIVERABLE ROADMAP

Work through this project in order.

Do not generate all deliverables at once.

## Deliverable 1: Repository Blueprint

Create:

- Recommended folder structure
- File descriptions
- Naming conventions
- README outline
- Rationale for each major folder
- Initial implementation plan

Do not create all phase content yet.

## Deliverable 2: Initial Repository Files

Create:

- README.md
- AI_GUIDELINES.md
- CONCEPTS.md starter
- docs/project-roadmap.md
- docs/repo-strategy.md

## Deliverable 3: Phase 0

Create:

- phases/phase-00-developer-workstation.md
- reviewer checklist for Phase 0
- reflection prompts for Phase 0
- demo checklist for Phase 0

## Deliverable 4: Printable Cheat Sheets

Create:

- cheatsheets/terminal-cheat-sheet.md
- cheatsheets/git-cheat-sheet.md

Design them to be printable front/back.

## Deliverable 5: GitHub Workflow

Create:

- .github/pull_request_template.md
- .github/ISSUE_TEMPLATE/phase-task.md
- .github/ISSUE_TEMPLATE/bug-report.md
- .github/ISSUE_TEMPLATE/question.md
- docs/github-workflow.md
- docs/branching-strategy.md

## Deliverable 6: Reviewer Guide

Create:

- docs/reviewer-guide.md
- docs/demo-guide.md
- docs/ai-coaching-guide.md

Make this practical for Ashley as parent/instructor/reviewer.

## Deliverable 7: Phase 1–3 Curriculum

Create detailed student phase files for:

- Phase 1: First Python Program
- Phase 2: Variables, Input, and Athlete Profile
- Phase 3: Conditionals and Goals

Include student guide, exercises, hints, demo checklist, reflection prompts, reviewer checklist, and AI usage suggestions.

## Deliverable 8: Phase 4–6 Curriculum

Create detailed student phase files for:

- Phase 4: Lists, Loops, and Multiple Results
- Phase 5: Functions and Cleaner Code
- Phase 6: CSV Files and Persistence

Include the same sections.

## Deliverable 9: Phase 7–8 Curriculum

Create detailed student phase files for:

- Phase 7: pandas Data Analysis
- Phase 8: Streamlit Phone-Friendly App

Include the same sections.

## Deliverable 10: Phase 9–10 Curriculum

Create detailed student phase files for:

- Phase 9: Deployment and Sharing
- Phase 10: Final Demo and Retrospective

Include the same sections.

## Deliverable 11: Starter App

Create beginner-friendly starter code only.

Files:

- app/README.md
- app/app.py
- app/data/sample_results.csv

Do not create the full final solution.

## Deliverable 12: Instructor Companion Repo Plan

Create a plan for a separate private instructor repository.

Suggested name:

programming-intro-python-bootcamp-instructor

It should eventually contain:

- Full solutions
- Reference implementations
- Phase rubrics
- Deeper reviewer notes
- Comparison checklists
- Common student mistakes
- Sample feedback
- Optional extension exercises

Do not put full answer keys in the public student repository.

---

# FIRST TASK

Start with Deliverable 1 only.

Generate the repository blueprint for programming-intro-python-bootcamp.

Include:

- Folder hierarchy
- File descriptions
- Naming conventions
- README outline
- Rationale
- Recommended first commits

Do not generate Deliverable 2 or later yet.
