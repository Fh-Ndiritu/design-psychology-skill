# 03 — Visual Communication

Governs how the eye is guided: hierarchy, anchors, distinction, grouping, and the signals that say "this is clickable."

---

### Establish hierarchy before placing a single element
- **Rule:** maximum three-level type scale per screen — primary (large, bold), secondary (medium, regular), tertiary (small, muted). Every text element belongs to exactly one level. Use color and weight contrast so interactive elements feel distinct from static ones.
- **Audit signal:** four+ competing type sizes/weights; clickable and readable text look identical; flat pages with no clear first/second/third read.
- **Guardrail:** hierarchy built for desktop often collapses on mobile — verify at every breakpoint.

### One dominant visual anchor per screen (Visual Anchors)
- **Rule:** give each screen a single high-contrast entry point the eye hits first. Place the primary CTA within its gravitational pull — touching or immediately below, never orphaned. Isolate it with whitespace.
- **Audit signal:** no clear entry point, or an anchor (big hero image) that draws the eye *away* from the user's goal.

### Make the single most important element visually singular (Von Restorff Effect)
- **Rule:** the "most-wanted action" gets one visual property no other element shares — color, size, shape, or motion. Enforce a strict one-highlight-per-screen rule.
- **Audit signal:** multiple highlighted/colored elements; two competing accent colors; a page where everything is emphasized (so nothing is).
- **Build move:** resist the urge to highlight secondary elements — every extra highlight steals from the primary one.

### Use proximity to declare relationship (Law of Proximity)
- **Rule:** elements that belong together sit together; distinct ones are separated. Form labels within 4–8px of their inputs. Trust signals adjacent to the action they support. Destructive actions physically separated from primary ones by a gap or divider.
- **Audit signal:** labels floating far from inputs; a security badge two scrolls from the buy button; delete next to save.

### Make every interactive element unambiguously interactive (Signifiers)
- **Rule:** buttons look like buttons at rest — filled or bordered, labeled, padded. In-text links carry ≥2 distinguishing properties (color + underline). Every interactive element has a visible focus state.
- **Audit signal:** flat "buttons" indistinguishable from text; links by color alone; missing hover/focus states; affordances hidden until hover.

### Make everything that behaves the same look the same (Law of Similarity)
- **Rule:** one visual signature per interaction type — primary, secondary, destructive, disabled — enforced by a component system, not per-screen discretion.
- **Audit signal:** the same action styled differently across screens; inconsistent button shapes/colors for the same role.

### Remove every element that doesn't serve the current goal (Selective Attention)
- **Rule:** on a focused task screen, apply a binary test to each element — does it directly help complete this step? If not, remove or defer it. Suppress persistent nav, promo banners, and recommendation widgets during checkout and critical forms.
- **Audit signal:** full nav and sidebars present during checkout; decorative elements with no function.

### Place highest-value content at the edges, not the middle (Serial Position Effect)
- **Rule:** in lists, nav, and benefit bullets, the most important item goes first (primacy), the second-most goes last (recency). The middle is the graveyard of attention.
- **Audit signal:** the killer differentiator buried mid-list; nav with the key destination in slot 3 of 5.
