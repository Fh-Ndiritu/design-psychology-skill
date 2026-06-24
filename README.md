# Design Psychology — a Claude skill

A portable [Claude](https://claude.com/claude-code) skill that audits or builds **any website or UI** against ~60 research-backed conversion and design-psychology principles — Hick's Law, Von Restorff, the Goal-Gradient Effect, Peak-End Rule, Fitts's Law, the Aha moment, loss aversion, social proof, feedforward, the labor illusion, and the rest.

It is **brand-agnostic**. It does not impose a style; it derives the target product's own tokens and voice, then applies the universal grammar on top. Point it at a live URL or a local codebase and it auto-detects which.

## Two modes

- **Audit** — review a live site or a repo and get a prioritized, located, fix-per-finding report scored by conversion/trust impact.
- **Build** — design or edit a screen, CTA, pricing table, onboarding flow, form, empty state, or error flow *through* the principles, with a rationale tying each decision to a named principle.

## Install

Claude skills are folders discovered from a skills directory. Drop this repo in (or symlink it):

```bash
# project-scoped
git clone https://github.com/<you>/design-psychology-skill .claude/skills/design-psychology

# or user-scoped (available in every project)
git clone https://github.com/<you>/design-psychology-skill ~/.claude/skills/design-psychology
```

The folder name becomes the skill name. Restart your Claude Code session (or re-scan skills) and it appears as `/design-psychology`.

## Use

```
/design-psychology audit https://example.com/pricing
/design-psychology review the onboarding flow in app/views/onboarding
/design-psychology build an empty state for the projects dashboard
/design-psychology critique this checkout screen and fix the top 3 issues
```

Or just describe the task — the skill triggers on review/build requests for any user-facing surface. See the model-facing instructions in [`SKILL.md`](SKILL.md).

## What's inside

```
SKILL.md                     ← orchestrator: modes, input detection, workflows, non-negotiables
references/
  00-principle-catalog.md     ← flat lookup: principle → definition → module
  01-conversion-architecture.md
  02-attention-and-decisions.md
  03-visual-communication.md
  04-trust-and-first-impressions.md
  05-motivation-and-retention.md
  06-simplicity-and-cognitive-load.md
  07-emotional-design.md
  08-memory-and-navigation.md
  09-honest-design.md          ← anti–dark-pattern rules; overrides any conflicting tactic
  10-visual-language-system.md ← the visual grammar, parameterized to the target's tokens
  11-meta-and-serp.md          ← title/description standard for SEO surfaces
checklists/
  audit.md                     ← final gate before reporting an audit
  build.md                     ← final gate before shipping a built surface
```

## Provenance

Distilled from a production design standard for a paid SaaS product, then generalized: brand specifics, fixed color tokens, and the paid-only business stance were removed so the principles apply to any product and any stack. The one business-model assumption that remains opt-out is noted in `SKILL.md` (free tiers/trials).

## License

MIT — see [`LICENSE`](LICENSE).
