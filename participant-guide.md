# Participant guide

## Mission

Test whether a skill improves the same AI model on the same coding task. This is a small controlled experiment, not an attempt to create a production-ready standard.

## Group roles

- **Driver:** operates the editor and Copilot.
- **Standard owner:** checks fidelity to the supplied rules.
- **Sceptic:** looks for ambiguity, leaks and counterexamples.
- **Recorder:** saves prompts, outputs, scores and observations.

## 1. Baseline

1. Select one file from `tasks/`.
2. Choose a language your group can review.
3. Start a fresh Copilot chat.
4. Use `templates/baseline-prompt.md`.
5. Give Copilot no standard, examples or skill.
6. Save the complete, uncorrected answer in `results/baseline.md`.

## 2. Analyse the evidence

Read `standard/safe-logging.md`, the relevant language examples and `examples/boundary-cases.md`.

Identify:

- observable rules;
- realistic mistakes shown by the counterexamples;
- cases where a simplistic rule would be wrong;
- checks that still require human judgement.

## 3. Generate and review the skill

Use `templates/skill-generation-prompt.md` and `templates/SKILL.template.md`. Save the result as `skills/safe-logging/SKILL.md`.

Before testing, remove requirements that the model invented and that are unsupported by the source material.

## 4. Run with the skill

1. Start a new chat.
2. Use `templates/skill-assisted-prompt.md`.
3. Paste exactly the same task and use the same language and model.
4. Save the complete, uncorrected answer in `results/with-skill.md`.

## 5. Blind peer evaluation

Exchange outputs with another group as Output A and Output B. Do not reveal which one used the skill. Reviewers use `evals/review-form.md` and record concrete code evidence for failures and unclear items.

## 6. Improve one thing

After revealing the runs, select the most important failure. Propose exactly one change to the standard, an example, the skill procedure or an evaluation criterion. Record it in `results/conclusions.md`.

## Definition of done

- baseline output;
- reviewed skill;
- skill-assisted output;
- blind peer evaluation;
- one evidence-based improvement proposal.
