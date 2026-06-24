# 06 — Simplicity & Cognitive Load

Governs how much mental effort a screen demands. The default move is subtraction.

---

### Strip every screen to its simplest legible form (Occam's Razor / Law of Prägnanz)
- **Rule:** remove every element, datum, and decision not necessary for the immediate task. Apply a binary test: what breaks if this is gone? Remove anything that survives. Write UI copy as the shortest grammatically complete sentence, then cut one more word.
- **Audit signal:** decorative elements with no function; copy padded with filler; information present "just in case."
- **Truth:** on focused task screens, subtraction consistently beats addition.

### Present no more than 5–7 choices per screen (Miller's Law)
- **Rule:** working memory holds ~5–7 items. Chunk related options under labeled headers so users scan groups, not items. Split forms >7 fields across steps. Limit primary nav to ≤5 items. Surface ≤3 pricing plans.
- **Audit signal:** long ungrouped option lists; forms with many fields on one screen; nav with 8+ top-level items.

### Break complex flows into named, bounded stages (Chunking)
- **Rule:** show a step indicator with *named* stages ("Account → Project → Publish"), not just numbered dots — names give a mental model of what's coming. Limit each step to a single decision or one category of related decisions.
- **Audit signal:** multi-step flows with no progress indicator, or dots with no labels; steps mixing unrelated decisions.

### Design each unit to be completable in under three minutes (Unit Bias)
- **Rule:** give each task a title, a visible boundary (card, modal, section divider), and an explicit completion state. Show the number of units upfront ("3 steps") so users calibrate effort before committing. Celebrate each unit's completion with a brief micro-interaction.
- **Audit signal:** unbounded tasks with no clear "done"; no upfront count of what's involved.

### Protect flow state above everything during active creation (Flow State)
- **Rule:** remove every interruption between starting and finishing a task. Collapse nav, toolbars, and secondary panels in an active creation/editing state. Replace modal interruptions (upsells, confirmations, update banners) with non-blocking inline alternatives during active work.
- **Audit signal:** upsell modals mid-task; banners interrupting creation; an interruption mid-generation (the highest-cost UX mistake).

### Absorb complexity into the system, not the user (Tesler's Law)
- **Rule:** complexity is conserved — someone bears it; make it the system. Set intelligent defaults for every field so a user can proceed without changing anything and still get a good outcome. Pre-fill known data (prior uploads, context, stated preferences). Never ask for information you already hold.
- **Audit signal:** required fields with no defaults; re-asking for data the system already has; configuration the system could infer.
