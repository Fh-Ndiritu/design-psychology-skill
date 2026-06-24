---
name: design-psychology
description: >-
  Audit or build any website/UI against research-backed conversion and
  design-psychology principles (Hick's Law, Von Restorff, Goal Gradient,
  Peak-End, Fitts's Law, the Aha moment, loss aversion, social proof,
  feedforward, labor illusion, and ~50 more). Use when reviewing a live URL or a
  local codebase for conversion/UX quality, or when designing or editing any
  user-facing surface — landing pages, pricing, onboarding, CTAs, forms, empty
  states, error flows, mobile screens. Auto-detects whether the target is a live
  URL or local source files. Brand-agnostic: derives the product's own tokens
  and voice instead of imposing a fixed style.
---

# Design Psychology

A portable standard for making interfaces that **convert on first contact, retain through genuine value, and feel premium** — grounded in ~60 named cognitive principles. It runs in two modes against any website, regardless of stack or brand.

This file is the orchestrator. It tells you *how to run*. The depth lives in [`references/`](references/), loaded on demand. Do not paste an entire reference file into your reasoning unless the task needs it — pull the specific principle.

---

## Two modes

| Mode | Trigger | Output |
| --- | --- | --- |
| **AUDIT** | "review / critique / score / improve this site/page/flow," a URL, a repo to evaluate | A prioritized findings report with severity, the violated principle, the exact location, and one concrete fix per finding. |
| **BUILD** | "design / build / write / redesign this screen / CTA / pricing / onboarding / empty state / error" | The artifact itself (markup, copy, component) produced *through* the principles, plus a short rationale tying each major decision to a principle. |

If the request is ambiguous, default to **AUDIT** when an existing surface is named, **BUILD** when a new artifact is requested. When both apply ("review and fix"), audit first, then build the fixes.

---

## Step 0 — Detect the input source (always first)

1. **A URL is present** → treat it as a live site. Capture what the user actually sees: use a screenshot/render tool if available (WebFetch for DOM + copy; a headless screenshot for layout/hierarchy/visual-quality judgments). Critique the *rendered* experience, not just the HTML. Note viewport: judge mobile and desktop separately — hierarchy that works on desktop routinely collapses on mobile.
2. **No URL, but you're in a repo / files are referenced** → read the source. Find the user-facing templates (`.html`, `.erb`, `.jsx/.tsx`, `.vue`, `.svelte`, Blade, Twig, etc.), the stylesheet/token layer (CSS, Tailwind config, design tokens), and the copy. Critique the source as it will render.
3. **Both available** → prefer the live URL for visual/hierarchy/perception judgments; use the source to locate the exact fix and to check tokens, defaults, and states (hover/focus/error/empty) that a single screenshot won't show.
4. **Neither** → ask for one (a URL, a repo path, or a screenshot). Do not invent a target.

Always state which source you used and at which viewport.

---

## Step 1 — Answer the Five Questions (gate for every surface)

Before auditing or building any single screen, answer all five. If you can't, you don't understand the screen yet — go look closer.

1. **Emotional state** — what is the user feeling when they arrive here?
2. **Single action** — what is the one thing they need to do?
3. **Perceived cost** — what does that action *feel* like it costs, in effort, risk, and time?
4. **Worst realistic case** — how does this hold up for a user who is stressed, rushed, on a small phone, mid-error?
5. **Memorable moment** — what will they remember about this in a week?

These five reframe every later finding. A "low contrast button" matters because of Q4; a "buried CTA" matters because of Q2.

---

## Step 2a — AUDIT workflow

1. **Frame the page's job.** One screen, one primary action (Step 1, Q2). Run the **squint test**: blur the page — does the single most important element dominate? If not, that's finding #1.
2. **Sweep the ten dimensions.** Walk each reference module against what's on screen. Don't quote the module — apply it. Each module ends with the failure modes that earn a finding.
   - [01 — Conversion architecture](references/01-conversion-architecture.md)
   - [02 — Attention & decision architecture](references/02-attention-and-decisions.md)
   - [03 — Visual communication](references/03-visual-communication.md)
   - [04 — Trust, polish & first impressions](references/04-trust-and-first-impressions.md)
   - [05 — Motivation, engagement & retention](references/05-motivation-and-retention.md)
   - [06 — Simplicity & cognitive load](references/06-simplicity-and-cognitive-load.md)
   - [07 — Emotional design & perception](references/07-emotional-design.md)
   - [08 — Memory & navigation](references/08-memory-and-navigation.md)
   - [09 — Honest design (anti–dark-pattern)](references/09-honest-design.md)
   - [10 — Visual language system](references/10-visual-language-system.md)
   - [11 — Meta titles & SERP (if SEO surfaces are in scope)](references/11-meta-and-serp.md)
3. **Score and prioritize.** Use the severity rubric below. Lead with what costs conversions, not what offends taste.
4. **Write one fix per finding.** Concrete and located: the element, the principle, the change. No finding without a fix.
5. **Run the audit-pass checklist.** [`checklists/audit.md`](checklists/audit.md) is the final gate before you report.

### Severity rubric

| Severity | Definition | Examples |
| --- | --- | --- |
| **Critical** | Directly blocks or leaks conversion; breaks a core flow; or is a dark pattern that will cause backlash/chargebacks. | No clear primary action; broken checkout; fake scarcity that resets; a "decline" that loops back. |
| **High** | Materially depresses conversion or trust but the flow still works. | Two competing accents (no Von Restorff anchor); CTA is a verb not an outcome; no social proof at the decision point; error states that blame the user. |
| **Medium** | Adds friction or cognitive load; erodes the premium feel. | Too many choices on one screen (Hick); inconsistent spacing scale; missing focus states; weak hierarchy. |
| **Low** | Polish and delight; safe to defer. | Missing a peak-moment micro-celebration; no easter-egg personality; sub-optimal but legible type scale. |

### Audit output format

```
## Design-psychology audit — <target> (<viewport/source>)

**Page job:** <one sentence — the single primary action>
**Five Questions:** <one line each, or a flag for any you couldn't answer>
**Squint test:** <pass/fail + what dominates>

### Findings (most costly first)
1. [CRITICAL] <Title> — <Principle>
   Where: <element / file:line / screenshot region>
   Why it costs: <the conversion/trust consequence>
   Fix: <one concrete change>
...

### What's already working
- <2–4 genuine strengths — never omit; it calibrates the critique>

### If you change one thing
<the single highest-leverage fix>
```

---

## Step 2b — BUILD workflow

1. **Answer the Five Questions for the screen you're about to make.** This sets the single action and the emotional register before any markup.
2. **Derive the brand's own design language — do not impose one.** Read the existing tokens (colors, spacing scale, type, radius, motion) from the codebase or infer them from the live site. The [visual language system](references/10-visual-language-system.md) gives you the *grammar* (one dominant accent, a surface ladder, glow-not-shadow depth, signature easing, component archetypes) — you fill it with *their* values. Never hardcode a specific hex or font; parameterize.
3. **Compose with the relevant modules.** Pricing/upgrade → 01 + 09. Onboarding → 02 + 05 + 06. Forms → 02 + 06 + 08. Error/empty states → 04 + 07 + 09. Visual styling of any of them → 10.
4. **Enforce the non-negotiables** (below) as you write.
5. **Run the build checklist.** [`checklists/build.md`](checklists/build.md).
6. **Hand back the artifact + a short rationale** mapping each consequential decision to its principle, so the choice is auditable.

---

## Non-negotiables (both modes)

- **One primary action per screen.** Name it before placing or judging a single element. If you can't, the screen is broken.
- **CTAs are outcome statements, not verbs.** "See your first result →" not "Submit."
- **Every default is a product decision** — and must serve the user, never the business at the user's expense. A default that benefits the company at the user's cost is a dark pattern.
- **Every gate needs a real exit.** Soft gates over hard blocks; a fake "decline" that loops is worse than none.
- **Design the worst moment as carefully as the best.** Error and empty states get the same craft as the success state — users judge a product by its worst screen (Negativity Bias).
- **Honesty is structural, not optional.** Module 09 overrides any conversion tactic that conflicts with it. Manufactured scarcity, fake social proof, hidden restrictions, and blame-the-user copy are bugs, not levers.
- **Accessibility is part of the standard.** ≥44×44px (web) / 48dp (native) targets; visible focus states; never convey state by color alone; AA contrast on body text; honor `prefers-reduced-motion`.

> **On free tiers / trials:** the source standard this skill is distilled from is for a paid-only product, so it forbids free tiers. That is a *business-model* stance, not a design law — when auditing or building for a product that legitimately uses a free tier or trial, keep the universal principle ("demonstrate the outcome before the commitment ask") and drop the paid-only rule. Don't flag a free trial as a violation.

---

## The principle catalog

Every rule here traces to a named cognitive principle. [`references/00-principle-catalog.md`](references/00-principle-catalog.md) is the flat lookup table — principle → one-line definition → primary module. Use it to (a) name the principle behind a finding precisely, and (b) jump to the module that elaborates it.

---

## Calibrate to the ask

Scale the work to the request. "Quick gut-check on this CTA" → Five Questions + the one or two relevant modules. "Full conversion audit of our funnel" → every module, scored, screen by screen, with an exit-point analysis (Module 09: measure failure as rigorously as success). Don't deliver a 30-finding report for a one-button question, and don't deliver a one-liner for "audit our pricing."
