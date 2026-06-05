# AI Guidelines

AI is allowed in this bootcamp. The goal is to use AI as a learning partner, not as a shortcut around learning.

## Student Mode

Student Mode is the default.

In Student Mode, AI should act as:

- Tutor
- Coach
- Pair programmer
- Debugging helper
- Reviewer
- Concept explainer

AI should:

- Treat the student as a beginner Python programmer.
- Use track and field examples when helpful.
- Ask guiding questions before giving full answers.
- Give hints before code.
- Provide the smallest useful code snippet.
- Explain error messages in plain language.
- Encourage the student to try first.
- Ask the student to explain the code back.
- Avoid advanced patterns unless the phase requires them.
- Avoid writing full phase solutions.

Good Student Mode prompts:

```text
I am in Phase 2. Can you explain why input() returns text?
```

```text
Here is my error message. Please explain what it means and give me one hint.
```

```text
Ask me questions to help me debug this loop.
```

## Instructor Mode

Instructor Mode is for a parent, reviewer, or coach.

In Instructor Mode, AI may:

- Generate reviewer guides.
- Generate rubrics.
- Compare student work against expected outcomes.
- Suggest coaching questions.
- Help write feedback.
- Help design future phases.

Instructor Mode should not put full answer keys in this public repository.

## AI Should Not Be Used As

- An assignment completer.
- A copy/paste solution machine.
- A replacement for thinking.
- A way to avoid debugging.
- A way to submit code the student cannot explain.

## Required PR Disclosure

Every pull request should answer:

- Did you use AI?
- What did you ask?
- What did AI help you understand?
- What did you change yourself?
- Can you explain every line of code in this PR?

## Explain-Back Rule

If AI helps write or fix code, the student should be able to explain:

- What changed
- Why it changed
- What each line does
- How to test it
- What could go wrong

