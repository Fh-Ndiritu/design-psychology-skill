# 01 — Conversion Architecture

Governs every moment a user is deciding whether to commit (sign up, pay, upgrade, start). The job: demonstrate the outcome before the ask, then make the right choice the obvious one.

> **Demonstrate before you ask.** The universal rule is to show the result the product produces — a finished output, a preview, a transformation — *before* the commitment ask. (Whether commitment means "pay" or "create an account" or "start a trial" depends on the business model; the demonstration comes first either way.)

---

### Lead with the outcome, never the feature list
- **Rule:** frame everything as what the user gains. Rewrite every limit/cost as a value statement. "Generate unlimited renders" beats "Removes the 3-render cap."
- **Audit signal:** copy that describes mechanics ("includes X, Y, Z"), negative framing of limits, or feature lists where a benefit should be.
- **Build move:** state the result first, the feature that delivers it second (if at all).
- **Guardrail:** never spin bad news into fake good news — positive framing that contradicts lived experience destroys trust faster than honest negatives.

### Show the product working before the price
- **Rule:** the strongest lever is a prospect who has already seen their problem solved. Use the first seconds of any landing/onboarding screen to show a specific, stunning result.
- **Audit signal:** pricing or signup asked for before any demonstration of the outcome; generic hero imagery instead of a real result.
- **Build move:** prime with a finished output, not the interface chrome.

### Anchor the highest-value option first
- **Rule (Anchoring):** lead with the premium option so everything else is judged relative to it. Show full price before any discount. Label the recommended option explicitly.
- **Audit signal:** cheapest plan shown first; no labeled recommendation; discount shown without the original.
- **Guardrail:** if the anchor reads as absurd, users disengage — it must be a tier real customers actually buy.

### Use a decoy to make the right choice obvious
- **Rule (Decoy Effect):** with 3+ options, position one to make the preferred one clearly superior by honest feature contrast. Visually elevate the target (border, badge, larger card).
- **Audit signal:** three plans with no contrast logic; the "best value" isn't visually distinguished.
- **Guardrail:** the decoy must be plausible enough that someone *could* pick it. Refresh it when pricing/features change — a stale decoy silently loses its effect.

### Put the preferred option center and last
- **Rule (Centre-Stage + Recency):** in a 3-column layout, the recommended plan goes in the visual center, loads/reveals last, leads its bullet list with the killer differentiator and closes with the second-strongest.
- **Audit signal:** recommended plan on an edge; strongest benefits buried in the middle of a bullet list.

### Pre-select the right default
- **Rule (Default Bias):** most users never change a default. Pre-select annual billing, the recommended plan, the common choice. Label defaults as recommended.
- **Audit signal:** no pre-selection, or a pre-selection that benefits the business at the user's expense (a dark pattern — see Module 09).

### Frame loss at decision points
- **Rule (Loss Aversion):** at abandonment, plan-consideration, and re-engagement, state what *disappears* in concrete terms. "Your projects and history require an active subscription" beats "Upgrade to keep access." Establish possession language ("your projects") consistently *before* the loss frame arrives.
- **Audit signal:** generic upgrade nags; no possession language; loss framing with no real loss behind it.
- **Guardrail:** the loss must be real and proportionate — overplayed loss triggers Reactance (Module 05/09).

### Surface genuine urgency only
- **Rule (Scarcity):** show real constraints (a genuine cohort cap, a real pricing window) at the moment of evaluation, with a specific number.
- **Audit signal:** countdowns that reset, "only 2 left!" that never changes, vague urgency words. Fake scarcity is immediately legible to repeat visitors and permanently discredits every future signal. **This is a Module 09 violation — flag as Critical.**

### Reduce payment friction to zero at the final step
- **Rule (Cashless Effect):** offer one-click / wallet payment (Apple Pay, Google Pay, Link). Post-purchase, confirm the exact amount, renewal date, and what was unlocked. Show a plain-language billing summary in settings.
- **Audit signal:** long card forms with no wallet option; ambiguous post-purchase state; no findable renewal terms.

### Pair difficult steps with immediate rewards
- **Rule (Temptation Bundling):** gate a compelling preview behind the hard step so finishing it triggers an immediate payoff. "See your first render" beats "Complete your profile."
- **Audit signal:** hard steps (profile setup, verification) with no reward on completion; rewards decoupled from the action that earns them (reads transactional).
