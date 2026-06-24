# 07 — Emotional Design & Perception

Governs how a product *feels* — its tone, its peaks and endings, its handling of waiting, and the immediacy of reward.

---

### Design the emotional tone with the same rigour as functional requirements (Affect Heuristic)
- **Rule:** choose a single emotional register (warm and encouraging, calm and precise) and apply it to every microcopy string, illustration, and interaction. Write errors in active, human language with a next step. Use microinteractions to signal care. Introduce warmth *before* the first commitment ask.
- **Audit signal:** inconsistent voice across screens; cold/robotic copy; no warmth before the ask.

### Engineer one peak and one satisfying ending into every flow (Peak-End Rule)
- **Rule:** an experience is remembered by its most charged moment and its end. Place a celebration at the functional peak — the moment the goal is achieved, not after. Design confirmation screens as genuine endings: a clear summary, a forward-looking prompt, a visual that signals closure. End cancellation/error flows on goodwill.
- **Audit signal:** the success moment passes with no acknowledgment; flows that just stop; confirmation screens that are dead ends.

### Insert one unexpected moment of personality per major flow (Delighters)
- **Rule:** write errors with empathy and occasional wit — "We dropped the ball — your work is safe, try again" beats "Something went wrong." Add a single micro-animation to the most-used action. Hide one easter egg to be discovered, never announced.
- **Audit signal:** inert generic errors; zero personality anywhere.
- **Guardrail:** delighters must be dismissible and invisible to users in a hurry — a cute animation blocking the primary action is a regression in costume.

### Make the system's work visible during every wait (Chronoception)
- **Rule:** fill unavoidable waits with information or motion that conveys forward progress. Replace indeterminate spinners with a meaningful percentage or step count. Use skeleton screens that load progressively, not blank states that snap. Set and communicate time estimates upfront.
- **Audit signal:** bare spinners; blank-then-snap loads; no time estimate.
- **Truth:** uncertainty, not duration, is the primary driver of abandonment.

### Make immediate use rewarding enough to justify the cost now (Hyperbolic Discounting)
- **Rule:** deliver a tangible output within the first interaction after commitment — a preview, a first result, a completed micro-task — so the user holds value before it fully unfolds. Frame future benefits in concrete near terms ("ready by Thursday"). Make progress toward long-term goals visible as a number/bar that changes after each interaction.
- **Audit signal:** nothing tangible delivered right after signup/payment; benefits framed abstractly/far-off.

### Frame the experience as a narrative arc (Storytelling Effect)
- **Rule:** write onboarding in second person, present tense, with a protagonist who has a problem and solves it — never a feature tour. Design empty states as chapter one: show what the screen looks like when full so users picture the future state. Replace stat-only proof with one vivid transformation story (who they were before, what changed, what they can do now).
- **Audit signal:** onboarding as a feature list; empty states that are dead ends; proof that's all numbers, no story.
