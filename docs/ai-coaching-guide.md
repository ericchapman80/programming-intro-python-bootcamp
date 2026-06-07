# AI Coaching Guide 🎯

Use AI to increase understanding, not to skip practice.

> [!TIP]
> The best AI session ends with the student saying, "I can explain this now."

For a high-level map of tool options, see [AI Tooling Landscape](ai-tooling-landscape.md).

## Coach Mindset

- Keep Riley in the driver's seat.
- Ask for reasoning before fixing code.
- Prefer one hint, one test, or one question at a time.
- Treat error messages as practice reps.
- Save full rewrites for instructor planning, not student submissions.

## Better Prompts

```text
Give me one hint about this bug.
```

```text
Ask me questions that help me debug this.
```

```text
Explain this error message like I am new to Python.
```

```text
Review my code for readability, but do not rewrite it yet.
```

```text
Quiz me on this function before suggesting changes.
```

```text
I want to solve this myself. Give me the next smallest step.
```

## Prompt Pattern

```text
I am in Phase __.
My goal is __.
Here is what I tried: __.
Here is the exact error or output: __.
Please give me one hint first, not the full solution.
```

## Reviewer Prompt

```text
You are in Instructor Mode. Review this Phase 3 pull request against the phase goals. Focus on coaching questions, missing understanding, and good enough to move on.
```

## Explain-Back Checklist

- I can describe what the code does.
- I can run it without help.
- I can explain the error messages I saw.
- I can make a small live change.
- I know what AI helped with.

> [!WARNING]
> If the student cannot explain code that AI produced, the code is not ready to submit.
