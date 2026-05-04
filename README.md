# ⚡ Claude Power Skills

> **80 battle-tested slash commands that turn Claude Code into a senior engineer, designer, and creative partner on your team.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Compatible-blue)](https://claude.ai/code)
[![Skills](https://img.shields.io/badge/Skills-80-green)](./commands)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

---

Most AI coding tools give you **what to do**. These skills give Claude **how to think**.

Each command is a structured workflow — not just a prompt, but a reasoning framework with explicit steps, checklists, and verification criteria.

---

## Why This Exists

Claude (and most LLMs) have three failure modes:

1. **Assumes instead of asks** — fills ambiguity with guesses, builds the wrong thing
2. **Over-engineers** — adds abstractions, patterns, and "future-proofing" nobody asked for
3. **Fixes symptoms** — patches the visible bug without finding the root cause

These skills fix all three by giving Claude explicit reasoning frameworks before it writes a single line of code.

---

## Skills

### Engineering (9 skills)

| Command | When to Use | What It Does |
|---|---|---|
| [`/think`](commands/think.md) | Before any complex task | 5-step deep analysis: understand → surface complexity → 3 approaches → recommend → success criteria |
| [`/ship`](commands/ship.md) | New features end-to-end | Clarify → plan → implement surgically → test → ship checklist |
| [`/debug`](commands/debug.md) | Bugs with unknown root cause | Reproduce → observe → hypothesize → eliminate → fix → prevent |
| [`/audit`](commands/audit.md) | Code review / security check | Correctness + security (OWASP) + performance + reliability |
| [`/refactor`](commands/refactor.md) | Improve code structure safely | Safety net first → small steps → verify behavior unchanged |
| [`/explain`](commands/explain.md) | Understand unfamiliar code | Big picture → data flow → design decisions → gotchas → safe modification |
| [`/test`](commands/test.md) | Write tests that catch real bugs | Happy path → edge cases → error cases → regression → quality check |
| [`/perf`](commands/perf.md) | Performance bottlenecks | Profile first → complexity analysis → bottleneck checklist → measure |
| [`/pr`](commands/pr.md) | Pull request creation | Diff review → title → description → test plan → self-review |

---

### Codebase Understanding (8 skills)
> Powered by [Understand-Anything](https://github.com/Lum1104/Understand-Anything)

| Command | What It Does |
|---|---|
| [`/understand`](commands/understand.md) | Analyze codebase via multi-agent pipeline → interactive knowledge graph |
| [`/understand-chat`](commands/understand-chat.md) | Ask questions about the codebase using the knowledge graph |
| [`/understand-dashboard`](commands/understand-dashboard.md) | Open interactive web dashboard to visualize the knowledge graph |
| [`/understand-diff`](commands/understand-diff.md) | Analyze impact of current changes before committing |
| [`/understand-explain`](commands/understand-explain.md) | Deep-dive explanation of a specific file or function |
| [`/understand-domain`](commands/understand-domain.md) | Extract business domain knowledge and generate domain flow graph |
| [`/understand-knowledge`](commands/understand-knowledge.md) | Analyze LLM wiki knowledge bases with topic clustering |
| [`/understand-onboard`](commands/understand-onboard.md) | Generate an onboarding guide for new team members |

---

### Design & Web (63 skills)
> Powered by [Open Design](https://github.com/nexu-io/open-design)

#### Web & UI
| Command | What It Does |
|---|---|
| [`/web-prototype`](commands/web-prototype.md) | General-purpose desktop web prototype |
| [`/web-prototype-taste-brutalist`](commands/web-prototype-taste-brutalist.md) | Swiss industrial-print web prototype |
| [`/web-prototype-taste-editorial`](commands/web-prototype-taste-editorial.md) | Editorial-minimalist web prototype |
| [`/web-prototype-taste-soft`](commands/web-prototype-taste-soft.md) | Apple-tier soft web prototype |
| [`/dashboard`](commands/dashboard.md) | Admin / analytics dashboard in a single HTML file |
| [`/saas-landing`](commands/saas-landing.md) | Single-page SaaS landing with hero, features, pricing |
| [`/pricing-page`](commands/pricing-page.md) | Standalone pricing page with plan tiers |
| [`/mobile-app`](commands/mobile-app.md) | Mobile-app screen rendered inside a pixel-perfect device frame |
| [`/mobile-onboarding`](commands/mobile-onboarding.md) | Multi-screen mobile onboarding flow |
| [`/dating-web`](commands/dating-web.md) | Consumer-feeling dating / matchmaking dashboard |
| [`/gamified-app`](commands/gamified-app.md) | Multi-frame gamified mobile-app prototype |
| [`/kami-landing`](commands/kami-landing.md) | Print-grade single-page kami-style landing |
| [`/open-design-landing`](commands/open-design-landing.md) | Open Design landing page |

#### Presentations & Decks
| Command | What It Does |
|---|---|
| [`/html-ppt`](commands/html-ppt.md) | HTML PPT Studio — professional static HTML decks |
| [`/html-ppt-pitch-deck`](commands/html-ppt-pitch-deck.md) | Investor-ready 10-slide pitch deck |
| [`/html-ppt-product-launch`](commands/html-ppt-product-launch.md) | Launch keynote deck |
| [`/html-ppt-weekly-report`](commands/html-ppt-weekly-report.md) | Team weekly / status-update deck |
| [`/html-ppt-tech-sharing`](commands/html-ppt-tech-sharing.md) | Conference / internal tech-talk deck |
| [`/html-ppt-course-module`](commands/html-ppt-course-module.md) | Online-course / workshop module deck |
| [`/html-ppt-taste-brutalist`](commands/html-ppt-taste-brutalist.md) | Tactical-telemetry / CRT-terminal style deck |
| [`/html-ppt-taste-editorial`](commands/html-ppt-taste-editorial.md) | Editorial-minimalist 16:9 deck |
| [`/html-ppt-graphify-dark-graph`](commands/html-ppt-graphify-dark-graph.md) | Dark knowledge-graph deck |
| [`/html-ppt-hermes-cyber-terminal`](commands/html-ppt-hermes-cyber-terminal.md) | Dark terminal honest-review deck |
| [`/html-ppt-obsidian-claude-gradient`](commands/html-ppt-obsidian-claude-gradient.md) | GitHub dark-purple gradient deck |
| [`/html-ppt-knowledge-arch-blueprint`](commands/html-ppt-knowledge-arch-blueprint.md) | Blueprint architecture deck |
| [`/html-ppt-xhs-post`](commands/html-ppt-xhs-post.md) | XiaoHongShu / Instagram 9-page vertical deck |
| [`/html-ppt-xhs-pastel-card`](commands/html-ppt-xhs-pastel-card.md) | Pastel macaron lifestyle deck |
| [`/html-ppt-xhs-white-editorial`](commands/html-ppt-xhs-white-editorial.md) | White editorial magazine deck |
| [`/html-ppt-dir-key-nav-minimal`](commands/html-ppt-dir-key-nav-minimal.md) | 8-page minimal arrow-key keynote |
| [`/html-ppt-presenter-mode-reveal`](commands/html-ppt-presenter-mode-reveal.md) | Presenter mode deck with tokyo-night theme |
| [`/html-ppt-testing-safety-alert`](commands/html-ppt-testing-safety-alert.md) | Red-amber hazard-stripe safety deck |
| [`/simple-deck`](commands/simple-deck.md) | Single-file horizontal-swipe HTML deck |
| [`/kami-deck`](commands/kami-deck.md) | Print-grade kami-style slide deck |
| [`/replit-deck`](commands/replit-deck.md) | Single-file HTML deck in Replit style |
| [`/open-design-landing-deck`](commands/open-design-landing-deck.md) | Atelier-style slide deck |
| [`/guizang-ppt`](commands/guizang-ppt.md) | Electronic magazine × e-ink style horizontal deck |

#### Content & Documentation
| Command | What It Does |
|---|---|
| [`/blog-post`](commands/blog-post.md) | Long-form article / blog post |
| [`/docs-page`](commands/docs-page.md) | Documentation page with left nav and scrollable content |
| [`/digital-eguide`](commands/digital-eguide.md) | Two-spread digital e-guide preview |
| [`/design-brief`](commands/design-brief.md) | Parse and render a structured design brief |
| [`/pm-spec`](commands/pm-spec.md) | Product spec / PRD as a single page |
| [`/eng-runbook`](commands/eng-runbook.md) | Engineering runbook with service overview and alerts |
| [`/meeting-notes`](commands/meeting-notes.md) | Meeting notes with attendees, agenda, and action items |
| [`/weekly-update`](commands/weekly-update.md) | Weekly team update slide deck |

#### Business & Marketing
| Command | What It Does |
|---|---|
| [`/email-marketing`](commands/email-marketing.md) | Brand product-launch email with masthead |
| [`/social-carousel`](commands/social-carousel.md) | Three-card social media carousel |
| [`/magazine-poster`](commands/magazine-poster.md) | Editorial-style newsprint poster |
| [`/image-poster`](commands/image-poster.md) | Single-image poster / key visual |
| [`/invoice`](commands/invoice.md) | Printable invoice page |
| [`/finance-report`](commands/finance-report.md) | Quarterly / monthly financial report |
| [`/hr-onboarding`](commands/hr-onboarding.md) | New-hire onboarding plan |
| [`/team-okrs`](commands/team-okrs.md) | OKR tracker page with quarter banner |

#### Tools & Utilities
| Command | What It Does |
|---|---|
| [`/critique`](commands/critique.md) | 5-dimension expert design review |
| [`/wireframe-sketch`](commands/wireframe-sketch.md) | Hand-drawn wireframe exploration |
| [`/kanban-board`](commands/kanban-board.md) | Kanban board with columns |
| [`/tweaks`](commands/tweaks.md) | Wrap any HTML artifact with a live-edit side panel |
| [`/pptx-html-fidelity-audit`](commands/pptx-html-fidelity-audit.md) | Audit a python-pptx export against its source |
| [`/hyperframes`](commands/hyperframes.md) | Video compositions, animations, title cards |
| [`/hatch-pet`](commands/hatch-pet.md) | Create, repair, validate, and preview pet assets |
| [`/sprite-animation`](commands/sprite-animation.md) | Pixel / sprite-style animated explainer |
| [`/motion-frames`](commands/motion-frames.md) | Single-frame motion-design composition |
| [`/audio-jingle`](commands/audio-jingle.md) | Audio generation for jingles, beds, voiceovers |
| [`/video-shortform`](commands/video-shortform.md) | Short-form video generation (3–10 seconds) |

---

## Installation

### Option 1: Global (recommended) — works in every project

```bash
git clone https://github.com/buihuudat/claude-power-skills.git
cp commands/*.md ~/.claude/commands/
```

### Option 2: Project-level — only for current project

```bash
mkdir -p .claude/commands
cp /path/to/claude-power-skills/commands/*.md .claude/commands/
```

Restart Claude Code. All commands are available immediately.

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

### `/understand` — Map any codebase instantly

```
/understand
```

Runs a 6-agent pipeline to scan, analyze, and build an interactive knowledge graph of your entire codebase. Outputs to `.understand-anything/knowledge-graph.json`.

### `/html-ppt` — Professional presentations in seconds

```
/html-ppt Q3 product review — growth metrics and roadmap
```

Generates a complete, styled HTML slide deck ready to open in any browser.

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

## Credits

- Engineering skills: original work inspired by [Andrej Karpathy's observations](https://x.com/karpathy) on LLM coding pitfalls
- Codebase understanding: [Understand-Anything](https://github.com/Lum1104/Understand-Anything) by Lum1104
- Design & web skills: [Open Design](https://github.com/nexu-io/open-design) by nexu-io

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). PRs welcome for:
- New commands (open an issue first to discuss)
- Better examples in [EXAMPLES.md](EXAMPLES.md)

---

## License

MIT — use freely, modify freely, credit appreciated.
