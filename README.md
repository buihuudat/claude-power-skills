# ⚡ Claude Power Skills

> **9 battle-tested slash commands that turn Claude Code into a senior engineer on your team.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Compatible-blue)](https://claude.ai/code)
[![Skills](https://img.shields.io/badge/Skills-9-green)](./commands)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

---

Most AI coding tools give you **what to do**. These skills give Claude **how to think**.

Each command is a structured workflow — not just a prompt, but a reasoning framework with explicit steps, checklists, and verification criteria. Inspired by [Andrej Karpathy's observations](https://x.com/karpathy) on LLM coding pitfalls, rebuilt from scratch with real-world engineering workflows.

---

## Why This Exists

Claude (and most LLMs) have three failure modes:

1. **Assumes instead of asks** — fills ambiguity with guesses, builds the wrong thing
2. **Over-engineers** — adds abstractions, patterns, and "future-proofing" nobody asked for  
3. **Fixes symptoms** — patches the visible bug without finding the root cause

These skills fix all three by giving Claude explicit reasoning frameworks before it writes a single line of code.

---

## Commands

| Command | When to Use | What It Does |
|---|---|---|
| [`/think`](commands/think.md) | Before any complex task | 5-step deep analysis: understand → surface complexity → 3 approaches → recommend → success criteria |
| [`/ship`](commands/ship.md) | New features end-to-end | Clarify → plan → implement surgically → test → ship checklist |
| [`/debug`](commands/debug.md) | Bugs with unknown root cause | Reproduce → observe → hypothesize → eliminate → fix → prevent |
| [`/audit`](commands/audit.md) | Code review / security check | Correctness + security (OWASP) + performance + reliability |
| [`/refactor`](commands/refactor.md) | Improve code structure safely | Safety net first → small steps → verify behavior unchanged |
| [`/explain`](commands/explain.md) | Understand unfamiliar code | Big picture → data flow → design decisions → gotchas → safe modification |
| [`/test`](commands/test.md) | Write tests that catch real bugs | Happy path → edge cases → error cases → regression → quality check |
| [`/perf`](commands/perf.md) | Performance bottlenecks | Profile first → complexity analysis → bottleneck checklist → measure improvement |
| [`/pr`](commands/pr.md) | Pull request creation | Diff review → title → description → test plan → self-review |

---

## Installation

### Option 1: Global (recommended) — works in every project

```bash
# Clone and copy commands
git clone https://github.com/buihuudat/claude-power-skills.git
cp commands/*.md ~/.claude/commands/
```

### Option 2: Project-level — only for current project

```bash
mkdir -p .claude/commands
cp /path/to/claude-power-skills/commands/*.md .claude/commands/
```

### Option 3: Claude Code Plugin (coming soon)

Add to your `~/.claude/settings.json`:

```json
{
  "extraKnownMarketplaces": {
    "claude-power-skills": {
      "source": {
        "source": "git",
        "url": "https://github.com/buihuudat/claude-power-skills.git"
      }
    }
  }
}
```

Then restart Claude Code. Commands are available immediately as `/think`, `/ship`, etc.

---

## Usage Examples

### `/think` — Stop Claude from assuming

```
/think refactor the payment service to support multiple currencies
```

Instead of immediately refactoring, Claude will surface: hidden complexity (exchange rates? rounding? existing transactions?), multiple approaches with tradeoffs, and concrete success criteria you can verify.

### `/debug` — Find root cause, not just symptoms

```
/debug login fails for users with uppercase emails on mobile
```

Claude won't just "try things." It reproduces the bug deterministically, generates ranked hypotheses with supporting/contradicting evidence, tests each one before touching code.

### `/audit` — Full code review in one command

```
/audit src/api/auth.ts
```

Returns severity-ranked findings across correctness, security (OWASP), performance, and reliability — with specific file:line references and suggested fixes.

---

## How These Compare to System Prompts

| | System Prompts / CLAUDE.md | Claude Power Skills |
|---|---|---|
| **Scope** | Always active, general behavior | Invoked when needed, task-specific |
| **Structure** | Guidelines (what to avoid) | Workflows (how to execute) |
| **Verification** | None | Explicit success criteria + checklists |
| **Flexibility** | Affects everything | Targeted — `/debug` for debugging, `/ship` for shipping |

**Recommendation:** Use both. Add the [CLAUDE.md](CLAUDE.md) behavioral guidelines to your project, then invoke specific skills for complex tasks.

---

## The Philosophy

> *"LLMs are exceptionally good at looping until they meet specific goals. Don't tell it what to do — give it success criteria and watch it go."* — Andrej Karpathy

These commands translate that insight into practice:
- **`/think`** converts vague requests into verifiable success criteria
- **`/debug`** converts "fix the bug" into "reproduce → hypothesize → prove"
- **`/ship`** converts "add feature X" into "clarify → checkpoint → verify"

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). PRs welcome for:
- New commands (open an issue first to discuss)
- Better examples in [EXAMPLES.md](EXAMPLES.md)
- Translations (see [README.vi.md](README.vi.md) for reference)

---

## License

MIT — use freely, modify freely, credit appreciated.
