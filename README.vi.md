# ⚡ Claude Power Skills

> **9 battle-tested slash commands that turn Claude Code into a senior engineer on your team.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Compatible-blue)](https://claude.ai/code)

---

## Why These Skills Exist

Claude (and most LLMs) have 3 failure modes:

1. **Assumes instead of asks** — fills ambiguity with guesses, builds the wrong thing
2. **Over-engineers** — adds abstractions, patterns, and "future-proofing" nobody asked for
3. **Fixes symptoms** — patches the visible bug without finding the root cause

These skills fix all three by giving Claude explicit reasoning frameworks before it writes a single line of code.

---

## Commands

| Command | When to Use | What It Does |
|---|---|---|
| `/think` | Before any complex task | 5-step analysis: understand → surface complexity → 3 approaches → recommend → success criteria |
| `/ship` | New features end-to-end | Clarify → plan → implement surgically → test → ship checklist |
| `/debug` | Bugs with unknown root cause | Reproduce → observe → hypothesize → eliminate → fix → prevent |
| `/audit` | Code review / security check | Correctness + security (OWASP) + performance + reliability |
| `/refactor` | Improve code structure safely | Safety net first → small steps → verify behavior unchanged |
| `/explain` | Understand unfamiliar code | Big picture → data flow → design decisions → gotchas → safe modification |
| `/test` | Write tests that catch real bugs | Happy path → edge cases → error cases → regression → quality check |
| `/perf` | Performance bottlenecks | Profile first → complexity analysis → bottleneck checklist → measure |
| `/pr` | Pull request creation | Diff review → title → description → test plan → self-review |

---

## Installation

### Global (recommended)

```bash
git clone https://github.com/buihuudat/claude-power-skills.git
cp commands/*.md ~/.claude/commands/
```

Restart Claude Code and use immediately.

### Project-only

```bash
mkdir -p .claude/commands
cp /path/to/claude-power-skills/commands/*.md .claude/commands/
```

---

## Real-World Example

### Without a skill (Claude guesses):
```
User: refactor payment service
Claude: [immediately starts refactoring with unconfirmed assumptions]
```

### With `/think` (Claude reasons first):
```
/think refactor payment service to support multiple currencies
Claude:
  Assumptions to confirm: where are exchange rates stored? Do existing transactions get affected?
  Approach A: wrapper layer (low risk, incremental deploy)
  Approach B: schema migration (clean, but requires downtime)
  Approach C: ...
  Success criteria: test X passes, behavior Y verifiable like this...
```

---

## License

MIT
