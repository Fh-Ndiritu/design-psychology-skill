# 08 — Memory & Navigation

Governs how little the interface asks users to remember, how it leans on images over text, and how it handles its worst moments and change.

---

### Surface every option so users never recall from memory (Recognition Over Recall)
- **Rule:** replace every free-text field that could be a dropdown, autocomplete, or recent-items list with one. Show recently visited projects/files/searches in a persistent, scannable list. Label every icon; never rely on shape alone. On confirmation screens, display all previously entered values so users verify without memory effort.
- **Audit signal:** free-text where a picker would do; unlabeled icons; confirmation screens that hide what was entered.

### Replace instructional text with visuals where possible (Picture Superiority Effect)
- **Rule:** audit every text-only tooltip/paragraph — "can this be shown?" If yes, show first and caption with text. Use icon-and-label pairs in navigation. Replace before/after explanations with side-by-side images. Use animated loops of the actual UI for walkthroughs, not static screenshots.
- **Audit signal:** walls of instructional text; explanations that should be demonstrations.

### Design error states with your best feature's craft (Negativity Bias)
- **Rule:** a single rough recovery outweighs ten smooth moments. Error messages name the problem specifically, explain why in plain language, and give exactly one clear next action. For delays >2s, show progress and signal control. After recovery, immediately confirm it with a positive micro-confirmation — close the emotional loop. Audit the five highest-traffic error states regularly; treat each as a product bug.
- **Audit signal:** vague errors; multiple or no next actions; no confirmation after recovery; neglected high-traffic error states.

### Seed the interface with vivid, recent, positive evidence (Availability Heuristic)
- **Rule:** surface recent positive outcomes ("Generated 3 renders for you today") so users have fresh favorable evidence when judging the product. After an error, follow up with a clear post-mortem naming what was fixed — silence leaves the negative memory uncontested. On trust pages, lead with specific, recent, concrete evidence.
- **Audit signal:** no surfacing of recent wins; silence after failures; trust pages with stale or vague claims.

### Introduce change in increments proportional to current magnitude (Weber's Law)
- **Rule:** roll out visual redesigns in phases (10% → 50% → 100%). Change price by no more than ~20–25% in a single move. Pair every significant UI change with a brief callout naming what changed and why. Preserve at least one major familiar anchor when overhauling a screen.
- **Audit signal:** big-bang redesigns with no explanation; large abrupt price jumps; nothing familiar left after a change.
