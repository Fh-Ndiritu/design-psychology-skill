# 04 — Trust, Polish & First Impressions

Governs the credibility a product earns in its first moments and keeps (or loses) through consistency, honesty of promises, and the quality of feedback.

---

### The first 50ms are the entire pitch (Aesthetic-Usability Effect)
- **Rule:** visual quality is judged in under 50ms and sets a baseline credibility score that persists all session. Enforce a spacing scale (4, 8, 16, 24, 32px), a tight palette (≈2 brand colors + one neutral scale + 3 semantic colors), and a consistent type hierarchy (one display, one heading, one body, one caption size).
- **Audit signal:** inconsistent spacing; >2 brand colors fighting; arbitrary type weights; the page "feels" cheap on first glance.
- **Truth:** users forgive small rough edges in a beautiful product; they never forgive a core flow that doesn't work.

### The first touchpoint sets credibility for everything (Halo Effect)
- **Rule:** invest disproportionately in the first screen a user sees — treat it as a brand asset. Make the fastest, most impressive result the first one they encounter. Fix performance on entry points first. Keep the visual language consistent across surfaces.
- **Audit signal:** a slow or unpolished landing/first-run; inconsistent design between marketing and app.

### Under-promise, over-deliver (Expectations Bias)
- **Rule:** add a modest buffer to every time estimate. Write feature copy that matches the current product, not the roadmap. Design error/empty states with the same care as success states.
- **Audit signal:** optimistic ETAs; copy describing unshipped features; neglected error/empty states.
- **Guardrail:** aim for a small positive gap, not systematic sandbagging — if *every* user is shocked it's good, acquisition copy is underselling.

### Keep every promise the interface makes (Cognitive Dissonance)
- **Rule:** the experience must match what every preceding screen implied. Audit each CTA label against the screen it leads to. Match tone and visual weight pre- and post-action. When the product changes, update upstream touchpoints simultaneously.
- **Audit signal:** a CTA that promises X and delivers Y; stale landing-page claims; tonal whiplash between screens.

### Show the outcome before they commit (Feedforward)
- **Rule:** make the consequence of a significant action visible before it's taken. CTAs are outcome statements: "Download as PDF," not "Submit." Preview next steps inline in multi-step flows. Show calculated consequences (cost, quantity, scope) adjacent to the confirm button.
- **Audit signal:** "Submit"/"OK"/"Continue" on consequential actions; cost/scope hidden until after confirmation.
- **Guardrail:** reserve feedforward for meaningful actions — trivial ones don't need previews.

### Place specific, credible social proof at the decision point (Social Proof / Bandwagon)
- **Rule:** specific numbers beat vague claims ("14,000 designers" > "thousands of pros"). Position testimonials adjacent to the action they support. Segment proof by the user's role/industry. Use authority signals (press, recognizable logos) as proof-by-association.
- **Audit signal:** vague proof; testimonials on a separate page from the CTA; one-size proof for every audience.
- **Guardrail:** fabricated/inflated proof destroys trust the instant it's detected. Low-volume authentic proof beats high-volume suspicious proof. (Module 09.)

### Use one specific person, not aggregated statistics (Singularity Effect)
- **Rule:** a single named, photographed, specific testimonial with a concrete before/after outweighs a page of polished quotes.
- **Audit signal:** stock photos, generic names, anonymous quotes — all destroy the effect instantly.

### Confirm every action within 200ms; never go silent (Feedback Loop)
- **Rule:** every action gets a visible, contextual response within ~200ms. For operations >1s, show a progress indicator with a stage label. Celebrate completion with a subtle confirmation. Inline validation fires on blur or after a 300–500ms typing pause — never on keydown.
- **Audit signal:** dead clicks; long operations with no progress; validation errors firing on every keystroke; no completion confirmation.

### Write for someone who has never used a tool like yours (Curse of Knowledge)
- **Rule:** write every label, tooltip, empty state, and step as if the reader has zero context. Replace jargon with plain language. Run a "stranger test." Use support-ticket phrasing as truth — if users ask "what does X mean?", that label is broken.
- **Audit signal:** internal jargon in UI; labels that assume product knowledge.

### Design for worst-case emotional conditions (Empathy Gap)
- **Rule:** high-stakes interactions must hold up for a stressed, tired, frustrated user. Error messages lead with the resolution, not the diagnosis. Break multi-step tasks into the smallest completable units so a stressed user can stop without losing progress. Cancellation and high-friction flows use calm, non-judgmental copy.
- **Audit signal:** error copy that leads with what went wrong; long uninterruptible flows; judgmental cancellation copy.
