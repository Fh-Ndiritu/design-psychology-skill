# 02 — Attention & Decision Architecture

Governs how many choices a screen presents, in what order, and how easy the important ones are to act on.

---

### One primary action per screen, always
- **Rule:** every screen has one job. Name the single most important action before placing or judging any element. Apply the **squint test** — blur the screen; the most important element must read as dominant.
- **Audit signal:** can't name the one action; multiple elements compete for "most important"; squint test has no winner.
- **Build move:** decide the primary action first, then build the hierarchy around it.

### Limit choices ruthlessly (Hick's Law)
- **Rule:** decision time grows with the number and complexity of options. Cap visible choices; collapse secondary actions behind "More"/overflow; group related options under labeled headers so users scan groups, not items. Pre-select the common choice. Show ≤3 pricing plans; hide edge tiers behind "see all plans."
- **Audit signal:** long flat option lists; >3 plans surfaced; every action at equal weight; no grouping.
- **Build move:** the right number of visible choices is usually fewer than you think.

### Show only what's needed for this step (Progressive Disclosure)
- **Rule:** reveal the next layer of information only when the user's action makes it relevant. Onboarding is a wizard. Advanced settings live behind a labeled toggle. Help appears on hover, not as permanent furniture. First-session onboarding covers only the single action needed to reach the first result.
- **Audit signal:** everything dumped on one screen; advanced options always visible; onboarding that teaches secondary features before the first win.
- **Guardrail:** experts must always have a clear path to skip ahead.

### Make every message native to the workflow, never a banner (Banner Blindness)
- **Rule:** users ignore anything that looks like an ad. Integrate prompts inline at the point of relevance. Trigger contextual messages only *after* a user action that makes them relevant — "You've generated 3 renders — here's what upgrading unlocks," never on page load.
- **Audit signal:** upsell banners on load; promo bars; anything that looks like an ad slot.

### Size and position targets by frequency and importance (Fitts's Law)
- **Rule:** time-to-target falls with size and nearness. Primary CTAs get the largest target (≥44×44px / 48dp), placed where the cursor/thumb naturally rests after the previous step. Use sticky/persistent CTAs on long pages.
- **Audit signal:** small or distant primary buttons; destructive actions adjacent to primary ones with no separation; CTA scrolled out of reach on long pages.
- **Guardrail:** destructive/irreversible actions need separation *and* a confirmation step — proximity must not become a liability.

### Front-load the most consequential decisions (Decision Fatigue)
- **Rule:** decision quality degrades with each prior decision. Sequence the consequential choices (plan, primary goal) first; push refinements (notifications, display name) last or out entirely. Set opinionated named defaults for every optional field so a user can complete setup by pressing "continue" without touching a toggle. Offer a "recommended" path that bypasses customization.
- **Audit signal:** trivial choices before the important ones; required fields with no defaults; no express path.
