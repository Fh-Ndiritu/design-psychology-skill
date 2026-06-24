# 09 — Honest Design (anti–dark-pattern)

These rules keep a product from becoming extractive. **They override any conversion tactic in Modules 01–08 that conflicts with them.** A persuasion technique that crosses into deception or coercion is a bug, not a lever — flag it as Critical in an audit, and never build it.

The test for every tactic: *does it help the user make a better-informed decision, or does it exploit them into a worse one?* The first is design; the second is a dark pattern.

---

### Explain every restriction transparently, never enforce silently (Streisand Effect)
- **Rule:** replace generic "You don't have access" screens with specifics — what's restricted, why, and what the user can do next. Display plan limits proactively *before* users hit them mid-task. Make change logs and policy updates findable and human-readable.
- **Audit signal:** opaque access walls; limits discovered only by hitting them; buried or unreadable policy changes.

### Write error messages in the system's voice, not the user's (Self-Serving Bias)
- **Rule:** replace accusatory validation ("You forgot to fill in this field") with system-owned language ("This field needs a value before we can continue"). On onboarding failure/dropout, assume the product wasn't clear enough, not that the user wasn't paying attention.
- **Audit signal:** "You" + blame in error copy; failure messaging that faults the user.

### Write copy that feels specific to the individual — honestly (Barnum-Forer Effect)
- **Rule:** reference the user's own content where possible ("Based on your last three uploads"). Write milestone copy that names the specific achievement ("You just published your first garden layout"), not generic celebration.
- **Guardrail:** personalisation that references data the user didn't knowingly provide reads as surveillance and erodes trust faster than generic copy. Only reference what they know they gave you.

### Measure failure as rigorously as success (Survivorship Bias)
- **Rule:** tag and analyze exit points with the same rigour as conversion points. Run exit surveys on *non-converting* users — their friction is invisible to those who converted. Audit onboarding for steps where new users drop but power users don't. When evaluating a change, ask: "what would the users who never came back say about this screen?"
- **Audit move:** in a full audit, include an exit-point analysis — where does this funnel most likely lose people, and is that loss even measured?

### Replace internal assumptions with sourced data (False-Consensus Effect)
- **Rule:** keep a live assumptions log; each assumption has a named source (user interview, analytics event, support-ticket cluster) or is flagged untested. Test copy on users unlike the team. Design for the most confused *and* the most expert user simultaneously — the "average user" often doesn't exist.
- **Audit signal:** design decisions justified by "users will obviously…" with no source.

### Map downstream behaviour before shipping any engagement mechanic (Second-Order / Cobra Effect)
- **Rule:** for each mechanic, write a "cobra check": what's the easiest way to game this reward without delivering the intended outcome? Instrument second-order signals (downstream churn, support tickets, user-reported stress) alongside the primary metric from day one. Default notifications to opt-in, not opt-out.
- **Audit signal:** engagement mechanics (streaks, badges, nags) with no thought to gaming or downstream harm; opt-out notifications.

---

## Dark-pattern blocklist (auto-flag as Critical)

- Fake or resetting scarcity/countdowns.
- Fabricated or inflated social proof, reviews, or user counts.
- A pre-selected default that benefits the business at the user's expense (pre-checked add-ons, hidden auto-renew upsells).
- A "decline"/"no thanks" that loops back to the same prompt, or is hidden/guilt-worded ("No, I don't want to save money").
- Hidden or obstructed cancellation; cancellation harder than signup.
- Costs, fees, or subscription terms revealed only after commitment.
- Forced continuity (a "free" trial that silently bills with no reminder).
- Confirmshaming, disguised ads, and bait-and-switch CTAs.
