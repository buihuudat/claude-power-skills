# Installation Guide

## Quick Install (30 seconds)

```bash
git clone https://github.com/YOUR_USERNAME/claude-power-skills.git
cp claude-power-skills/commands/*.md ~/.claude/commands/
```

Restart Claude Code. Type `/think`, `/debug`, etc.

---

## Verify Installation

In Claude Code, type `/` — you should see the new commands in the autocomplete list.

Or run:
```bash
ls ~/.claude/commands/
# Should show: think.md  ship.md  debug.md  audit.md  refactor.md  explain.md  test.md  perf.md  pr.md
```

---

## Installation Options

### Global (all projects)
Commands installed at `~/.claude/commands/` are available in every project.

```bash
cp commands/*.md ~/.claude/commands/
```

### Project-only
Commands at `.claude/commands/` (in your project root) are only available in that project.

```bash
mkdir -p .claude/commands
cp /path/to/claude-power-skills/commands/*.md .claude/commands/
```

### Selective install
Only want specific commands?

```bash
# Just /debug and /audit
cp commands/debug.md commands/audit.md ~/.claude/commands/
```

---

## Adding CLAUDE.md Behavioral Guidelines

For best results, also add the behavioral guidelines to your project:

```bash
# Append to existing CLAUDE.md
cat /path/to/claude-power-skills/CLAUDE.md >> ./CLAUDE.md

# Or copy as new file
cp /path/to/claude-power-skills/CLAUDE.md ./CLAUDE.md
```

---

## Updating

```bash
cd claude-power-skills
git pull
cp commands/*.md ~/.claude/commands/
```

---

## Uninstall

```bash
rm ~/.claude/commands/think.md \
   ~/.claude/commands/ship.md \
   ~/.claude/commands/debug.md \
   ~/.claude/commands/audit.md \
   ~/.claude/commands/refactor.md \
   ~/.claude/commands/explain.md \
   ~/.claude/commands/test.md \
   ~/.claude/commands/perf.md \
   ~/.claude/commands/pr.md
```
