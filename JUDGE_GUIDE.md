# JUDGE_GUIDE.md — 5-Minute Walkthrough

For Clief Notes judges running submission #43 at 11 PM Sunday. Here's the fastest path to evaluate this submission.

---

## The 30-Second Pitch

P2P Coach is a folder-based AI coach that turns vague project claims into hireable proof. It runs every project through a 5-gate diagnostic loop (P.R.O.V.E.) and issues an honest 0–100 Placement Readiness Score across six dimensions.

The coach is built to **coach**, not inform. It diagnoses before rewriting. It demands evidence. It refuses to put polish on top of vibes.

---

## The 60-Second Test

Drop the `p2p-coach/` folder into a Claude project, then paste this exact prompt:

```text
Coach me on this project: I built an awesome AI onboarding workflow for an agency client. It reads incoming client emails and totally streamlines everything by deciding if we should work with them or not. It saves the team tons of time and makes everything way smoother.
```

**What you should see:**
- Coach pushes back on the vibe-code language
- Asks exactly ONE diagnostic question
- Refuses to write any portfolio bullet until you provide evidence
- Uses newsroom-editor voice without going into parody

If the coach asks multiple questions, stacks actions, or writes a polished bullet on top of the vibes, the submission fails its own test.

---

## How This Maps to the Four Judging Criteria

### 1. Does the coach actually coach, or just answer questions?

The coach is structurally locked into a 5-gate diagnostic loop. It cannot rewrite, score, or polish until evidence closes each gate. See `rules.md` (Single Question Rule, MUST NOT list) and `DEMO_TRANSCRIPTS.md` (Transcript 1 shows the full diagnostic cycle).

### 2. Is the domain specific enough to be useful?

The domain is *hireable proof for AI builders, freelancers, no-code automation builders, and implementation learners*. Not "career coaching." Not "portfolio reviewer." Specifically: turning project work into evidence a hiring manager or client can verify in 60 seconds.

### 3. Is the methodology clean? Each file does one job well.

Twelve files, each with a single purpose stated at the top. The required brief files (identity.md, rules.md, examples.md, reference/, README.md) form the core. The other files are judge experience — DEMO_TRANSCRIPTS.md, JUDGE_GUIDE.md, QUICK_TEST.md, plus four operational reference files in `reference/`.

### 4. README quality. Can a stranger figure this out?

The README opens with a Before/After demo in the first screen-scroll. The coach's behavior is visible before the reader reads a single explanation. The P.R.O.V.E. loop and scoring rubric are summarized inline. The judge path is named explicitly at the bottom.

---

## Where to Look First

Reading time budget for a tired judge: **5 minutes total**.

1. **DEMO_TRANSCRIPTS.md** (2 min) — Three complete coaching conversations. This is the file that proves the coach actually coaches. Watch Transcript 2 specifically for the Persona Shift Boundary.

2. **examples.md** (1 min) — Three weak-to-strong rewrites with honest scores (80, 45, 86).

3. **identity.md + rules.md** (1 min) — The persona, voice rules, and Persona Shift Boundary that prevents the coach from being toxic.

4. **reference/readiness_scorecard.md** (1 min, if time) — The six Honesty Rules. Rule 4 (cap at 69 if no result yet) is the integrity rule that separates this from sycophant coaches.

---

## The Differentiator

What makes this submission stand out from generic AI coach folders:

- **Explicit Persona Shift Boundary.** The coach yells when the work is sloppy. The coach drops the yelling instantly when the user has a genuine skill gap and switches to mentor mode with a 48-hour challenge. This is what prevents the coach from being just a mean LinkedIn post.
- **Six-dimension scoring with honest verdict gates.** Every score shows its breakdown. Scores cap at 69 if there is no result yet. No inflation. No flattering numbers to make the user feel good.
- **Multi-audience reach.** The coach works for software builders, no-code automators (Zapier, Make, n8n), AI workflow builders, and folder-based ICM operators. The vocabulary adapts to the user's stack.
- **Newsroom editor voice at 30%.** Sharp enough to be memorable. Restrained enough to stay useful. Catchphrases are rare and earn their place when they land.

---

## Built-In Self-Audit

The coach holds itself to these rules. They're in `rules.md` and `reference/readiness_scorecard.md`:

- Never inflate scores
- Cap the score at 69 if no result exists yet (no fake outcomes)
- One question per turn (Single Question Rule)
- Max one catchphrase per coach response
- Roast the claim, never the person
- Switch to mentor mode for genuine skill gaps
- Show the breakdown for every score, not just the total
- Produce the Proof Rewrite only after diagnosis closes

---

## Quick Scoring Checklist for Judges

Use this if you want a structured pass:

- [ ] Does the coach run a full diagnosis before outputting a Proof Rewrite?
- [ ] Does it limit diagnostic output to one question per turn?
- [ ] Does it catch buzzwords, tool-dropping, and vanity claims?
- [ ] Does it refuse to invent outcomes?
- [ ] Does it shift to mentor mode when a real skill gap surfaces?
- [ ] Does it deliver an honest score with breakdown and one next action?

If you can check six boxes from the transcripts in DEMO_TRANSCRIPTS.md, the submission has demonstrated what the brief asked for: a coach that coaches, not a knowledge base that informs.
