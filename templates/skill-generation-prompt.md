# Skill-generation prompt

```text
Create a concise reusable coding-agent skill from the supplied standard, examples, counterexamples and boundary cases.

The skill must preserve the standard's meaning and priority; state its triggers and exclusions; guide generation and review; define a short procedure; identify common failure modes; include an observable self-review checklist; explain what to do when sensitivity is unknown; avoid invented framework rules; and avoid copying all examples.

Use the supplied template. Keep the result short enough to read during a code change.

STANDARD:
[paste standard/safe-logging.md]

EXAMPLES:
[paste one or more files from examples/]

BOUNDARY CASES:
[paste examples/boundary-cases.md]

TEMPLATE:
[paste templates/SKILL.template.md]
```
