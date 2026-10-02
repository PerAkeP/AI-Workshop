# AI Skill Workshop: Safe logging

A two-hour, language-flexible workshop that tests whether a smaller GitHub Copilot model produces code that follows a coding standard more consistently when it receives a reusable skill built from rules, examples and counterexamples.

## Hypothesis

> The same model, on the same task, will require less manual correction when given a focused skill with observable rules and a self-review procedure.

## Learning goals

Participants will:

1. turn a prose standard into observable rules;
2. distinguish examples, counterexamples and boundary cases;
3. generate and review an agent skill;
4. compare baseline and skill-assisted output;
5. evaluate code independently of the model's explanation.

## Quick start

1. Read `participant-guide.md`.
2. Choose one task in `tasks/` and a language the group can review.
3. Run the task without the standard or skill. Save it in `results/baseline.md`.
4. Study `standard/` and `examples/`.
5. Generate `skills/safe-logging/SKILL.md` with the supplied template and prompt.
6. Run the unchanged task in a fresh chat with the skill. Save the answer in `results/with-skill.md`.
7. Exchange anonymised outputs with another group and use `evals/review-form.md`.
8. Record conclusions and one proposed improvement.

## Experimental rules

- Use the same task, language and model in both runs.
- Start a fresh chat for each run.
- Do not show the baseline answer to the skill-assisted run.
- Do not repair generated code before evaluation.
- Judge code evidence, not confident explanations.
- Mark an item `Unclear` instead of guessing.

## Repository structure

```text
standard/     Source coding standard
examples/     Good, bad and boundary cases
tasks/        Language-neutral coding tasks
templates/    Ready-to-paste Copilot prompts and skill template
skills/       Group workspace
evals/        Blind review and unseen facilitator challenge
results/      Generated outputs and conclusions
```

No build tools, containers or local models are required.
