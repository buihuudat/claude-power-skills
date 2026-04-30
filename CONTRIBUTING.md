# Contributing

## Adding a New Command

1. Open an issue first — describe the use case and why existing commands don't cover it
2. Fork the repo, create a branch: `git checkout -b add-command-NAME`
3. Create `commands/NAME.md` following the structure below
4. Add a real example to `EXAMPLES.md`
5. Update the table in `README.md`
6. Submit a PR

## Command Structure

Every command must have:

```markdown
# /name — One-line description

What this does and when to use it: $ARGUMENTS

---

## Step 1: [Name]
- Concrete actions, not vague guidance
- Specific checks or questions to ask

## Step 2: [Name]
...

## Final Output
What Claude should produce at the end
```

**Quality bar:**
- Steps must be actionable (not "think about the problem")
- Must include explicit verification (how do you know it worked?)
- Must prevent at least one specific LLM failure mode
- Must have a real example in EXAMPLES.md

## Improving Existing Commands

- Better examples are always welcome
- If a step is vague, make it concrete
- If a step is redundant, remove it

## Translations

Add `README.LANG.md` (e.g., `README.zh.md`, `README.ja.md`). Keep it in sync with the English README structure.
