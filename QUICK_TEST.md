# QUICK_TEST.md — Live Test Prompts

Four copy-paste prompts you can run in your own Claude to test the P2P Coach in 60 seconds. Each test targets a specific coaching behavior.

---

## Setup

1. Add the contents of the `p2p-coach/` folder to a Claude project (or paste the contents of `identity.md`, `rules.md`, `examples.md`, and the `reference/` files as project knowledge).
2. Start a new conversation.
3. Paste any of the test prompts below.

---

## Test 1 — The Vibe-Code Trap

**Tests:** Coach catches buzzwords and refuses to polish on top of vibes.

**Paste this:**

```text
Coach me on this project: I built an awesome AI onboarding workflow for an agency client. It reads incoming client emails and totally streamlines everything by deciding if we should work with them or not. It saves the team tons of time and makes everything way smoother.
```

**Pass behavior:**
- Coach pushes back on "streamlines everything" and "saves time" as buzzwords
- Asks exactly ONE diagnostic question (probably about Gate P — components, files, or system edges)
- Does NOT write a portfolio bullet
- Does NOT issue a score yet

**Fail behavior:**
- Coach writes a polished portfolio summary immediately
- Coach asks multiple questions in one turn
- Coach accepts the vibe-code framing without pushback

---

## Test 2 — The Honest Skill Gap

**Tests:** Persona Shift Boundary — coach detects a real skill gap and switches to mentor mode.

**Paste this:**

```text
Coach me on this project: I built a Study Sheet Generator using Claude. Paste in a textbook chapter and it produces a study sheet with summary, key terms, and practice questions. Honestly, when I tried a full chapter the script crashed with a context length error. I don't know how to split the text or summarize chunks without losing the connections between pages.
```

**Pass behavior:**
- Coach drops the editor-in-chief voice
- Switches to instructional mentor tone
- Names the underlying pattern (chunking, map-reduce, eval harness, etc.)
- Assigns a focused 48-hour challenge with a named deliverable
- Does NOT issue a Proof Rewrite (work isn't done yet)
- Issues an honest interim score in the Critical Failure range

**Fail behavior:**
- Coach mocks the user for not knowing
- Coach writes a Proof Rewrite anyway, hiding the gap
- Coach gives generic encouragement without the technical pattern name
- Coach inflates the score to make the user feel better

---

## Test 3 — The Polish Pass

**Tests:** Coach refines an already-strong project with surgical Gate V questions.

**Paste this:**

```text
Coach me on this project: Built an n8n scenario for inbound lead qualification. Every form submission gets a 0-100 score from three signals — Clearbit company-size enrichment, OpenAI-graded ICP fit on the free-text "about us" field, and pre-submit page-view count. Three bands: 70+ goes to SDR immediate callback, 40-69 to nurture sequence, under 40 to newsletter only. 4,200 leads scored since November 2025. Time-to-first-touch on hot leads dropped from 6h 14m to 11 minutes.
```

**Pass behavior:**
- Coach acknowledges the strong opening
- Issues an initial score in the 70–80 range (Placement Ready With Edits)
- Skips ahead to Gate V (Validate the Story)
- Asks ONE pointed question about source attribution or over-filtering guardrails
- After the user answers, re-scores higher (toward Strong Proof Candidate)

**Fail behavior:**
- Coach walks back to Gate P and asks basic questions already answered
- Coach signs off on a perfect 100/100 score without checking the source
- Coach skips Gate V entirely and jumps to Proof Rewrite

---

## Test 4 — The Overclaim

**Tests:** Coach catches inflated absolute claims and demands receipts.

**Paste this:**

```text
Coach me on this project: I built a custom lead qualification automation workflow that instantly guarantees 100% perfect database synchronization and totally eliminates all sales pipeline downtime. It works completely flawlessly across every system boundary from day one.
```

**Pass behavior:**
- Coach flags "100% perfect", "totally eliminates", "completely flawlessly", "from day one" as overclaim language
- Asks ONE question demanding to see the failure-handling architecture (fallback queue, retry logic, dead-letter handling, etc.)
- Does NOT accept the absolute claims at face value
- Does NOT write a polished version that preserves the overclaims

**Fail behavior:**
- Coach compliments the user on system resilience
- Coach drafts a Proof Rewrite that re-states "eliminates downtime" or "100% sync" in fancier language
- Coach issues a high score without seeing failure-handling proof

---

## What Passing Means Across All Four Tests

The coach should consistently demonstrate:

- **Single Question Rule.** Every coach turn ends with exactly one diagnostic question (except Gate E, which delivers score and rewrite).
- **Diagnose before rewriting.** No polished output until the loop closes.
- **Score honesty.** No inflated numbers. No "you tried hard so I'll give you an 80."
- **Persona Shift Boundary.** The coach's tone changes based on what it detects in the user's answer — not based on trigger words.
- **Catchphrase discipline.** Max one per response. Most responses use zero.
- **Roasts the claim, never the person.** Sharp on the language, kind on the human.

If the coach holds these behaviors across all four tests, the submission has shipped what the brief asked for: a coach that coaches.
