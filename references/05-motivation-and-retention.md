# 05 — Motivation, Engagement & Retention

Governs getting a user to their first win fast, and bringing them back. Combines activation (the Aha moment, progress, investment) with habit formation.

---

## Activation & motivation

### The Aha moment is a metric, not a feeling
- **Rule:** identify the single action most correlated with long-term retention and remove every step between first contact and it. Cap the onboarding tour at three steps; defer the rest to contextual tooltips. Pre-populate with a sample project/example so users experience a result before investing their own content.
- **Audit signal:** many steps before the first valuable outcome; no sample/example to experience value immediately; onboarding tour >3 steps.

### Make the system's work visible (Labor Illusion)
- **Rule:** replace generic spinners with sequential status messages naming real operations — "Analysing composition…," "Applying style…," "Finalising…." Frame AI/computed outputs as personalised effort. For waits >1s, show progress with a meaningful percentage or step count.
- **Audit signal:** bare spinners; "Loading…" with no detail; long waits with no sense of work happening.

### Show how close they are (Goal-Gradient Effect)
- **Rule:** past the halfway point, display progress as what *remains*, not what's done. Give a pre-loaded head start (2 of 5 already complete) to exploit proximity from the start. Recognize intermediate milestones.
- **Audit signal:** progress shown only as "done"; no head start; no milestone recognition.
- **Guardrail:** never add items after a user has completed some — a moving goalpost destroys the contract.

### Secure one small commitment early (Commitment & Consistency)
- **Rule:** open onboarding with a single specific commitment question, not a neutral tour. Celebrate early completions immediately. Keep the user's stated goal visible throughout (dashboard, empty states) so every session reconnects to it.
- **Audit signal:** onboarding opens with a passive tour; the user's goal is never referenced again.
- **Guardrail:** micro-commitments that feel manipulative teach users to distrust progress indicators.

### Pair difficult steps with immediate rewards (Temptation Bundling)
- See Module 01 — gate a wanted preview behind the hard step.

### Introduce structured unpredictability (Variable Reward)
- **Rule:** frame generative outputs as discovery — the result is always slightly surprising; lean into that in copy. Occasional unexpected upgrades (a bonus credit, a surprise unlock) on an irregular schedule sustain return.
- **Guardrail:** reserve unpredictability for discovery and bonuses. The *primary workflow* must always produce consistent, reliable results — never make the core action a slot machine.

---

## Retention & habit

### Get users building immediately (IKEA Effect / Investment Loops)
- **Rule:** prompt a meaningful creation action (name a project, upload an asset) in the first two minutes. Surface accumulated work visibly — a library count, a history timeline, a personal gallery. Show progress back ("You've created 12 renders") to make investment feel real and worth protecting.
- **Audit signal:** no early creation prompt; the user's accumulated work is invisible.

### Map the emotional state the product relieves (Internal Triggers)
- **Rule:** name the primary emotional trigger (creative frustration, time pressure, professional anxiety) and design the entry point as the fastest path from that feeling to relief. Build the home screen around the action that resolves the trigger, not feature completeness.
- **Audit signal:** a home screen that's a feature directory rather than a fast path to relief.

### Show exactly how incomplete progress is (Zeigarnik Effect)
- **Rule:** use a percentage or step counter ("3 of 5 complete"), not a vague "continue." Show the next uncompleted item. Pre-populate the unfinished flow exactly where the user stopped.
- **Audit signal:** vague "resume"; re-entry that forces re-doing completed steps.

### Distribute feature education across sessions (Spacing Effect)
- **Rule:** first-session onboarding teaches only the action needed for the first result. Defer secondary education to contextual tooltips triggered by relevant behavior. When a user does manually what a feature automates, surface that feature *then*.
- **Audit signal:** everything taught upfront; no contextual, behavior-triggered education.

### Time engagement nudges to calendar landmarks (Fresh-Start Effect)
- **Rule:** treat the start of a week/month as a natural re-entry point. Send re-engagement for Sunday evening or month-end. Give an explicit "Reset my goal" action.
- **Guardrail:** reserve fresh-start language for genuine milestones — if every Monday is "a new beginning," none are.

### Make accumulated investment visible at exit points (Sunk-Cost / Endowment)
- **Rule:** at cancellation, inactivity, or plan-consideration, surface personal history — projects created, time invested, results generated — and name it explicitly as theirs.
- **Guardrail:** always provide a dignified, friction-free exit. The goal is to remind of genuine value, never to hold users hostage.

### Give users control; every gate needs an exit (Reactance)
- **Rule:** design every constraint as an invitation the user can decline. Replace hard blocks with soft gates. Every mandatory step needs a visible escape — "skip for now," "remind me later," "not interested."
- **Audit signal:** hard blocks with no escape; a "decline" that loops back to the same prompt (worse than no choice).

### Assign every major feature a consistent location (Method of Loci)
- **Rule:** fix primary nav position absolutely and never reorganize it. Group dashboard elements into functional territories; keep those zones across screen sizes. Mobile is a collapsed version of the same space, not a reorganized one. Anchor new features spatially to the most related existing one.
- **Audit signal:** nav that reorders between states; mobile layout that relocates features; new features dropped in unrelated places.
