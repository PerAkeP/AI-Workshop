# Skill-assisted prompt

Use a fresh chat:

```text
Follow the coding skill below while implementing the task. Apply only relevant rules. If a security-relevant detail is unspecified, choose the safer minimal implementation and state the assumption briefly.

SKILL:
[paste skills/safe-logging/SKILL.md]

TASK:
[paste exactly the baseline task]

Use the same language and model as the baseline. Return compact, understandable code. Then list at most three assumptions and perform the skill's self-review using concrete code evidence.
```
