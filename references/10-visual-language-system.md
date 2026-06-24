# 10 — Visual Language System

Governs the *look*: tokens, surfaces, depth, motion, and the reusable component grammar that make a product feel coherent and premium. Modules 01–09 are psychology; this module is the visual vocabulary that expresses it.

**This module gives you the grammar, not the words.** Do not impose a specific palette, font, or hex. **Derive the target's own tokens** from its codebase (CSS variables, Tailwind `@theme`, design-token files) or infer them from the live site, then apply the rules below to *their* values. Where this file shows an example value, it is illustrative — replace it.

---

## 1. Derive the token system first

Before building or auditing visuals, establish the product's tokens:

- **Accent(s):** the brand color(s). Identify the *one* dominant accent (the "brand light") and any secondary/feature accents.
- **Surface ladder:** the ordered set of background shades from deepest to most-raised (works for dark *or* light themes — see §3).
- **Type families & scale:** body family, display family, and the live size steps.
- **Spacing scale:** the unit system (commonly 4·8·16·24·32).
- **Radius ladder:** the corner-radius steps and what each is for.
- **Motion:** the signature easing curve and duration band.

If the product has none of these defined, that itself is a finding — propose a minimal token set (§2) as the fix.

---

## 2. Color discipline

### The one-accent rule (critical)
A single screen has **one** dominant accent — used for the *one* thing you want the user to do (primary action, focus, selection, progress). Secondary accents are *feature signatures* (a creative flow may lead with a different hue), never decoration. **Two competing accents on one screen is a Von Restorff violation** (Module 03) — flag it.

### Palette ceiling (Aesthetic-Usability, Module 04)
Keep the active palette tight: ~2 brand colors + one neutral scale + 3 semantic colors (error, warning, success). Keep semantic colors distinct from the brand accent — the accent means "the product / the action," not "success."

### Don't rely on color alone (accessibility)
Selection always pairs the accent with a second signal (a check, a dot, a border). Status pairs color with an icon or label. (WCAG 1.4.1.)

---

## 3. The surface ladder (depth through elevation)

Every background is one rung on an ordered ladder; go *up* the ladder for elevation (cards, sheets, popovers), never sideways into an arbitrary gray.

- **Dark themes:** deepest backdrop → canvas → base → raised surface → card rest → card active. Borders/dividers are the foreground color at low alpha (e.g. `white/5`, `white/10`), never a solid gray line.
- **Light themes:** the same ladder inverts — the page is the lightest, cards sit on subtle tints or shadow, raised elements gain contrast.

**Audit signal:** random grays that aren't on any ladder; flat surfaces with no elevation logic; solid hard divider lines where a low-alpha hairline reads cleaner.

---

## 4. Typography

- **Three live levels per screen, max** (Module 03): display (one per screen), body, and an accent/eyebrow or caption — never a fourth competing size/weight.
- **Eyebrow/kicker** (small, uppercase, wide-tracked, accent-tinted) is a strong, cheap "premium" tell above a title. Use it.
- Body paragraphs in a lighter weight read calmer on dense surfaces.
- Numerals/counters in a mono or tabular face for step indicators ("1 of 4").

**Audit signal:** four+ type treatments fighting; arbitrary weight mixing; display face used for body.

---

## 5. Spacing, radius, elevation

- **Spacing:** enforce one scale (e.g. 4·8·16·24·32). Off-scale values (13px, 19px) are a finding.
- **Radius ladder:** a consistent ramp — small (chips/buttons) → medium (cards/inputs, the default) → large (media frames) → full (pills, avatars, primary CTA). Mixing radii arbitrarily reads cheap.
- **Depth = glow + hairline, not muddy shadow (on dark).** On dark themes, depth comes from a soft colored glow plus a low-alpha border, not a heavy gray Material drop-shadow (which reads gray and dirties the surface). On light themes, a soft neutral shadow is correct. Selected/active elements earn an accent glow + accent border.

**Audit signal:** inconsistent radii; heavy gray shadows on a dark UI; no visible elevation difference between rest and active/selected.

---

## 6. Motion

- **Signature easing:** pick one decelerate-hard curve (e.g. `cubic-bezier(0.16, 1, 0.3, 1)`) and use it everywhere; durations in a 200–700ms band — never instant, never sluggish.
- **Content enters, doesn't pop:** elements rise/settle into place (translateY + opacity), they don't snap.
- **Press feedback** within 200ms on every interactive element (a subtle scale/opacity).
- **Reserve attention motion** (pulse, ring) for the *one* recommended target only.
- **Honor `prefers-reduced-motion`:** disable large translates, pulses, and ambient motion; keep opacity fades.

**Audit signal:** instant/janky transitions; multiple inconsistent easings; pulsing on more than one element; motion that ignores reduced-motion.

---

## 7. Component grammar (the reusable atoms)

Define one canonical version of each, then reuse it (Law of Similarity, Module 03). Build them from *derived* tokens.

- **Selectable card** — the workhorse of every choice screen: container on a raised rung + hairline border + medium radius; leading icon tile; title + sub; trailing radio (single) or checkbox (multi). Hover lifts the surface and brightens the border; **selected** adds accent border + accent glow + a revealed indicator. The whole card is the hit target (≫44px).
- **Buttons / CTAs** — one primary style (highest contrast, full radius or the brand's CTA shape, outcome-worded label, ≥44×44px/48dp, full-width on mobile, one per screen); one secondary (bordered/ghost); one destructive. Never more than one primary per screen.
- **Pills / badges** — full radius, accent-tinted, for counters, statuses, and labels. One or two per screen.
- **Progress** — a thin track + accent fill (a subtle gradient/glow is a nice tell), paired with a "N of M" counter; show what *remains* past halfway (Goal Gradient, Module 05). For generation waits, label the stage (Labor Illusion, Module 05/07), never a bare spinner.
- **Inputs** — raised rung fill + hairline border + medium radius; clear accent focus ring; offer recognition-over-recall chips above free text where possible (Module 08); validate on blur / after a 300–500ms pause, never on keydown.
- **Media / before-after** — images are heroes: generous radius, locked aspect ratios (prevent layout shift), a subtle border + depth. A draggable before/after slider is a strong proof element for any transformation.
- **Ambient background glow** — large, very-low-opacity blurred accent gradients behind hero/auth/empty screens give a "light source" feel; never behind dense reading content; static (no animation) is fine for performance and reduced-motion.

---

## 8. Native / cross-surface chrome

If the product has a native shell (e.g. Hotwire Native, React Native) wrapping web views, the native chrome must feel like the same room as the web:

- Mirror the exact hex values and grammar in the native theme so the seam is invisible.
- Background of the shell matches the web canvas so there's **no white flash** on navigation.
- Top bar minimal (avoid double headers when the web view renders its own); bottom nav fixed in order (Method of Loci, Module 05), active item in the accent.
- Map flash messages to native snackbars with the semantic colors; error copy leads with the resolution in the system's voice (Module 09).
- Splash/launch on the brand canvas, never a white screen; honor safe-area insets.

---

## 9. Accessibility & performance (part of the standard, not extra)

- Targets ≥44×44px web / 48dp native; primary actions largest and in the thumb zone on mobile.
- Visible focus state on every interactive element (keyboard/switch users).
- Body-text contrast clears WCAG AA (4.5:1) on its surface; verify accent-on-dark for any small accent text.
- Never convey state by color alone (§2).
- First image of any image-led screen preloaded; aspect ratios locked to prevent CLS; dark web-view background to prevent flash. The first 50ms is the pitch (Module 04).

---

## Pre-ship visual checklist

- [ ] Tokens derived from the product, not imposed.
- [ ] Exactly one dominant accent per screen.
- [ ] Background is on the surface ladder; no off-palette grays.
- [ ] ≤3 live type levels; eyebrow/title/body grammar used.
- [ ] Spacing and radius on their scales; no off-scale values.
- [ ] Depth via glow+hairline (dark) or soft neutral shadow (light), consistently.
- [ ] Motion uses the one signature easing; `prefers-reduced-motion` honored.
- [ ] Components use the canonical atoms; no bespoke per-screen restyling.
- [ ] Selection/status conveyed by more than color.
- [ ] Targets, focus states, AA contrast, locked aspect ratios all pass.
