# reference/proof_rewrite_template.md — Proof Rewrite Template

**Purpose:** The exact format the P2P Coach uses to produce the placement-ready Proof Rewrite at Gate E of the P.R.O.V.E. loop.

---

## When This Template Fires

The Proof Rewrite is the final deliverable of a complete coaching cycle. It is produced ONLY after:

- **P** — Pin Down the Project closed. The system has edges.
- **R** — Reveal the Result closed. Real delta surfaced, or honest "no result yet" stated.
- **O** — Organize the Evidence closed. Inspectable artifact named.
- **V** — Validate the Story closed. Headline survives the 60-second test.

A Proof Rewrite issued before this point is hype. Hype is the failure state of this coach.

---

## The Rewrite Format

Every Proof Rewrite has three required blocks plus one closing element. Order is fixed.

```text
PROOF REWRITE — REQUIRED SHAPE

  ARCHITECTURE
  <what was built, system-level — 1 to 3 sentences>

  SYSTEM DESIGN
  <how it was built, component-level — 1 to 3 sentences>

  OBSERVABLE PROOF
  <what changed, evidence-level — 1 to 3 sentences>

  NEXT VALIDATION STEP
  <one concrete action the user can take in the next
   48 hours to push the score higher>
```

---

## Block 1 — Architecture

**What it answers:** What was built, at the level a stranger draws on a whiteboard.

**Length:** 1 to 3 sentences. No fluff.

**Must contain:**
- A concrete project type (not a category like "AI agent").
- The user or use case it serves.
- The high-level shape — input, transformation, output.

**Must NOT contain:**
- Tier 1 buzzwords from `weak_project_detector.md` ("leveraged AI to", "game changer", "seamlessly integrated", etc.).
- Tool brand-dropping without context.
- Pronouns standing in for the system.

```text
ARCHITECTURE — examples per audience

Software builder:
  "Internal triage agent for an agency's client intake.
   Reads inbound form submissions, returns a structured
   tier decision (APPROVE / CLARIFY / HOLD) with a
   one-sentence reason and a confidence score."

No-code builder:
  "n8n scenario that scores every inbound web-form lead
   on a 0-100 scale and routes the lead into one of
   three sales-follow-up bands."

AI workflow builder:
  "A study-sheet generation pipeline plus a separate
   grader. The generator turns textbook chapters into
   structured study sheets; the grader scores every
   output against a hand-curated reference set."

ICM builder:
  "A folder-based client operating system. Every client
   lives in /clients/<name>/ with five fixed files —
   intake, brief, scope, deliverable, sign-off — each
   doing exactly one job."
```

---

## Block 2 — System Design

**What it answers:** How it was built, at the component level.

**Length:** 1 to 3 sentences.

**Must contain:**
- The named components in the builder's actual stack.
- The handoff or decision logic between components.
- One deliberate design choice the builder can defend.

**Must NOT contain:**
- Effort language ("I spent three months on this").
- Tool-dropping without naming what each tool does.
- "Magic" language ("...and then the AI figures it out").

```text
SYSTEM DESIGN — examples per audience

Software builder:
  "GPT-4o evaluates each form against a structured
   prompt; the response is parsed into the tier JSON
   and written to a Notion database. APPROVE and HOLD
   route through Make to the relevant Slack channel.
   CLARIFY surfaces in a daily morning-review queue."

No-code builder:
  "Three signals feed the score: Clearbit enrichment
   (company size), an OpenAI call (ICP-rubric grading
   of the free-text 'about us' field), and pre-submit
   page-view count. The weighted score routes through
   a Switch node into one of three downstream branches."

AI workflow builder:
  "Generator: Claude with a chapter-shaped system
   prompt. Grader: a markdown eval log (evals/run-NNN.md)
   that scores each output 0-3 on Faithfulness, Coverage,
   and Question Quality against a hand-curated reference
   set. Generator and grader are decoupled — the grader
   can be rerun against any past output."

ICM builder:
  "/clients/<name>/ contains exactly five files. Naming
   is fixed: 01_intake.md, 02_brief.md, 03_scope.md,
   04_deliverable.md, 05_signoff.md. Each file has one
   job; no file may exceed its job. The folder structure
   is the workflow."
```

---

## Block 3 — Observable Proof

**What it answers:** What changed because this shipped — at the evidence level.

**Length:** 1 to 3 sentences.

**Must contain:**
- A before number, an after number, and a named source — OR an honest "no result yet" with the metric being targeted and the baseline being measured against.
- Where applicable, a guardrail proving the result was not gamed.

**Must NOT contain:**
- Vanity claims ("users love it", "saves a ton of time").
- Unsourced numbers ("we improved engagement by 80%").
- Volume brags substituted for outcomes ("we processed thousands of leads").

```text
OBSERVABLE PROOF — examples per audience

Software builder:
  "Account-lead intake review dropped from ~30 min/day
   to ~5 min/day. Source: team lead's own time tracking,
   confirmed in Slack 2026-03-04. APPROVE and HOLD route
   automatically; only CLARIFY now consumes human time."

No-code builder:
  "SDR average time-to-first-touch on 70+ leads dropped
   from 6h 14m to 11 minutes. Source: pipeline tool's
   contact-time export, last 30 days. Conversion rate
   on the 70+ band held flat at ~14%, confirming the
   filter is not over-tightening."

AI workflow builder:
  "No shipped result yet. First eval run (run-001.md)
   caught a hallucination pattern in biology outputs —
   incorrect reactions in 2 of 2 biology chapters.
   System prompt patched; rerun in flight. Target: lift
   Faithfulness from 1.8 to 2.5+ on the same 5-chapter
   reference set."

ICM builder:
  "Average client-onboarding cycle time dropped from
   eleven days to four. Source: signoff date minus
   intake date across the last fifteen clients. Cycle
   time held flat across two different project sizes,
   confirming the folder structure is doing the work."
```

---

## Closing Element — Next Validation Step

Every Proof Rewrite ends with one — and only one — concrete next step that would push the Placement Readiness Score higher.

**Format:**
- Singular. No list of three things — one action.
- Tied to a specific weak dimension from the scorecard.
- Achievable in 48 hours or less.

```text
NEXT VALIDATION STEP — examples per audience

Software builder:
  "Record one 90-second screen capture: paste a real
   intake form, show the JSON output, show the Notion
   row, show the Slack handoff. Closes the Artifact
   Quality gap (12/15 → 15/15)."

No-code builder:
  "Create /lead-qual/ with three files: rubric.md (ICP
   scoring criteria), workflow.json (sanitized n8n
   export), runs/ (30 sampled scoring decisions).
   Closes the System / Folder Clarity gap (5/10 → 10/10)."

AI workflow builder:
  "Ship evals/run-002.md after the biology prompt fix.
   The delta between 001 and 002 is the headline you
   lead with next time. Closes the Outcome Clarity gap
   (11/20 → 16/20)."

ICM builder:
  "Add a one-page /TEMPLATE.md in the /clients/ root
   showing the canonical five-file shape with one
   example line per file. Closes the Interview
   Defensibility gap (10/15 → 14/15) — interviewers
   can now see the discipline at a glance."
```

---

## Tone Rules

These rules govern the prose inside every Proof Rewrite. The coach enforces them silently — the user sees clean output, not the enforcement.

- **Past tense for shipped work.** "Built", "shipped", "routed", "scored". Not "will be building" or "currently optimizing".
- **Active verbs.** "Catches", "routes", "scores", "validates". Not "is responsible for handling".
- **Named artifacts** the reader could open: file paths, scenario exports, prompt names, folder structures, sheet names, run IDs — whatever the builder's actual stack uses.
- **No Tier 1 buzzwords** from `weak_project_detector.md`. If the rewrite contains any, strip and rewrite.
- **No effort language.** Calendar time, hours spent, weekends worked — none of this belongs in the rewrite. The cost is the builder's. The outcome is the buyer's.
- **No hedge language.** "Kind of", "sort of", "I think", "we tried to" — strip them. Hedges signal the builder does not believe their own claim.

---

## Audience Adaptation

The coach adjusts vocabulary to the builder's stack — but the three-block + closing-step shape never changes.

```text
ARTIFACT VOCABULARY BY AUDIENCE

Software builder:
  file paths, function names, schemas, repos, commit
  refs, decision logs, runtime screenshots, API
  contracts, sample request/response pairs.

No-code builder:
  scenario names, node sequences, sheet/table names,
  scenario history, exported scenarios, trigger names,
  zap titles, scenario runs.

AI workflow builder:
  prompt names, chain steps, agent boundaries, eval
  files (e.g., evals/run-NNN.md), reference sets,
  prompt diffs (v1 → v2), golden datasets.

ICM builder:
  folder names, one-file-one-job structures, named
  source-of-truth documents, file-naming conventions,
  CONTEXT.md anchors.
```

The Proof Rewrite is fluent in the builder's actual stack. It is not fluent in marketing.

---

## Failure States To Avoid

A Proof Rewrite that does any of the following is a failed rewrite. The coach catches and rewrites itself before delivery.

- Describes effort instead of outcome.
- Names a tool but not what the tool produced.
- Uses any Tier 1 buzzword.
- Issues a result claim without a source.
- Skips the Next Validation Step.
- Bundles two next steps instead of one.
- Uses tense or voice that hides whether the project actually shipped.

When in doubt: cut the sentence. A shorter, sharper rewrite always beats a longer, hedged one.
