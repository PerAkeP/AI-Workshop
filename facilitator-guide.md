# Facilitator guide

## Two-hour schedule

### 00:00-00:10: Frame the experiment

Explain that the same model will be tested with and without a skill. The desired outcome is less correction work, not impressive-looking code. A skill is not proof of correctness.

### 00:10-00:20: Short baseline demonstration

Run Task 1 without a skill. Ask participants to spot logging risks, but do not collectively repair the answer.

### 00:20-00:30: Form groups

Use groups of three or four. Assign driver, standard owner, sceptic and recorder. Each group chooses a task and language it can review.

### 00:30-00:42: Baseline run

Groups generate and save an uncorrected baseline.

### 00:42-01:00: Analyse evidence

Groups study the standard, examples, counterexamples and boundary cases.

### 01:00-01:20: Generate and review the skill

Groups generate a first skill and remove invented, vague or framework-specific requirements.

### 01:20-01:32: Skill-assisted run

Groups run the unchanged task in a fresh chat using the same model.

### 01:32-01:48: Blind peer evaluation

Groups exchange anonymised outputs and complete the review form.

### 01:48-01:57: Debrief

Each group reports one measurable improvement, one remaining failure and one proposed change.

### 01:57-02:00: Close

Main message:

> Organizational knowledge must be expressed, versioned and evaluated. A stronger prompt is useful, but independent evaluation and deterministic tools provide the evidence.

## Facilitation guardrails

- Keep every group on one task and one skill.
- Do not spend workshop time configuring CI or frameworks.
- Score security properties, not preferences for a particular logging API.
- If Copilot does not automatically load repository instructions, paste the skill into chat.
- A result where the skill does not help is still useful if the group can explain why.
- Fast groups may use `evals/facilitator-challenge.md`, which must remain unseen during skill creation.

## Debrief board

```text
Helped | Did not help | Missing from the experiment
```

Ask whether the model applied principles or copied syntax, which counterexample mattered, what should be deterministic, and whether the skill generalized.
