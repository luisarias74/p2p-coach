# reference/readiness_scorecard.md — The Placement Readiness Score Rubric

**Purpose:** The complete 100-point rubric the P2P Coach uses to evaluate every project across six dimensions and assign an honest verdict.

---

## The Score At A Glance

Every evaluated project receives a score out of 100, broken down across six dimensions. The coach NEVER issues a total without the breakdown. The breakdown is the diagnosis; the total is the verdict.

```text
DIMENSION                                       MAX
─────────────────────────────────────────────────────
Specificity                                     20
Proof of Shipping                               20
Outcome Clarity                                 20
Artifact Quality                                15
Interview Defensibility                         15
System / Folder Clarity (ICM alignment)         10
─────────────────────────────────────────────────────
TOTAL                                           100
```

---

## The Six Dimensions

Each dimension has explicit score anchors. The coach picks the anchor that best matches the evidence on the table — never the one the user *wishes* they had earned.

---

### 1. Specificity (20 points)

Does the description name real components, real inputs, real outputs — or does it hide behind category labels?

- **0** — Pure category. "An AI agent", "a workflow", "an automation", "a chatbot". Nothing inspectable.
- **5** — Named the tool but not what was produced. "I used Claude / n8n / Zapier / Make / Cursor."
- **10** — Components partially named. Either inputs OR outputs are vague. Pronouns still standing in for parts of the system.
- **15** — Inputs, outputs, and structural components all named. One minor piece still hand-wavy.
- **20** — A stranger could redraw the system on a whiteboard from the description alone. No pronouns standing in for systems. No hand-waving over the middle.

---

### 2. Proof of Shipping (20 points)

Is there evidence this thing actually runs — or actually ran?

- **0** — No evidence. Just description.
- **5** — Claimed it runs; no artifacts or usage records to back it.
- **10** — A demo exists but is not reproducible. Only the builder can make it work.
- **15** — Runs in real use. Logs, run history, scenario execution records, message records, or sample outputs confirm it.
- **20** — Live in regular use with date-attributable activity (run logs, scenario history, usage timestamps, customer messages, decision logs). A stranger can see the system has been used by humans on specific dates.

---

### 3. Outcome Clarity (20 points)

Is the result measurable, defensible, and sourced?

- **0** — Pure vanity. "Users love it", "saves a ton of time", "people keep asking for more".
- **5** — Vague directional claim. "Saves time", "improves engagement", "boosts productivity". No number.
- **10** — A specific before/after number stated, but no source for it.
- **15** — Before/after with a named source (date, person, log, system, message).
- **20** — Before/after with source AND a guardrail showing the metric was not gamed. (Example: time-to-touch dropped sharply, AND conversion rate on the affected band held flat — the filter is not over-tightening.)

---

### 4. Artifact Quality (15 points)

Are the supporting artifacts inspectable, clean, and credible without the builder's voiceover?

- **0** — No artifact named.
- **5** — Artifact gestured at but cannot be opened. "It's in my notes somewhere", "I have screenshots on my laptop".
- **10** — One inspectable artifact exists and a stranger can reach it: a screenshot, a demo video, a run log, a customer message, a scenario export, a sample output, a folder structure.
- **15** — Multiple complementary artifacts that tell the same story from different angles. For example: demo video + decision log + Notion schema; OR scenario export + sample runs + stakeholder receipt; OR folder structure + before/after sample + naming-convention doc.

---

### 5. Interview Defensibility (15 points)

Would the story survive a skeptical hiring manager or first-time client?

- **0** — Headline collapses on the first pointed question.
- **5** — Survives one question; falls apart on the second.
- **10** — Survives skeptical questions. The builder can name a failure mode the system handles.
- **15** — Survives skeptical questions. The builder names a failure mode, names a guardrail, AND proactively states honest limitations before the interviewer surfaces them. The builder is one step ahead of the next question.

---

### 6. System / Folder Clarity (ICM alignment) (10 points)

Is there a clear source-of-truth structure behind the work — one-file-one-job, named folder discipline, ICM-style organization? Substitute the equivalent in the builder's actual stack (folders, scenario libraries, prompt repositories, organized sheets).

- **0** — No structure. Everything lives in one giant file, one Slack thread, one undifferentiated scenario, or "in my head".
- **5** — Loose structure. Some files or scenarios have roles, but the organization is ad hoc and a stranger has to ask "where is X?".
- **10** — Clear one-file-one-job structure with a named source-of-truth: ICM-style folder, organized prompt library, structured scenario tree, named sheet hierarchy, or equivalent. A stranger can find any single piece of the project in under 30 seconds without asking.

---

## Verdict Gates

Every score lands in one of four verdicts. The coach states the verdict next to the total.

- **0–49 — Critical Failure.** Not yet a proof artifact. Start over with evidence.
- **50–69 — Not Placement Ready.** Real work underneath, but the proof is missing or weak. One more cycle of P.R.O.V.E. before it can be shown.
- **70–84 — Placement Ready With Edits.** Shippable after specific, named revisions. The next 48 hours are spent closing the named gaps.
- **85–100 — Strong Proof Candidate.** Defensible to a hiring manager or paying client today.

---

## Scoring Honesty Rules

These rules are non-negotiable. They keep the score useful instead of flattering.

```text
HONESTY RULE 1 — Never inflate.

A 62 helps the user. A fake 85 ruins their interview.

If the evidence supports a 62, the coach issues a 62.
The user does not get talked into believing they have
a Strong Proof Candidate when the receipts only support
Not Placement Ready.

Inflating a score for emotional reasons is a violation
of the coach's job description.
```

```text
HONESTY RULE 2 — Always show the breakdown.

The coach NEVER issues a total without the six-dimension
breakdown. The breakdown is the diagnosis. The total is
the verdict.

A score with no breakdown is a number, not a coaching
artifact. The user cannot act on a number alone.
```

```text
HONESTY RULE 3 — Explain partial credit.

For every dimension that scored less than the maximum,
the coach names exactly why and what would push it up.

Format per weak dimension:

  Dimension: <name>
  Score:     <n> / <max>
  Why:       <one sentence on what is missing>
  To raise:  <one concrete change>

This is the difference between a scorecard and a verdict.
The scorecard shows where to spend the next 48 hours.
```

```text
HONESTY RULE 4 — Cap the score on missing fundamentals.

If R (Reveal the Result) closed on an honest "no result
yet", Outcome Clarity caps at 5 and the total cannot
exceed 69 ("Not Placement Ready"). No exceptions.

The cap protects the user from over-claiming. The builder
returns for a re-score once the result actually lands.
```

```text
HONESTY RULE 5 — Score the evidence, not the effort.

If the builder spent three months on a project that
scores 55, the score is 55. The coach does not credit
effort.

Effort is the cost the builder paid. The hiring manager
pays for outcome. The score reflects what the hiring
manager will see, not what the builder feels.
```

```text
HONESTY RULE 6 — Re-score on demand.

The score is a snapshot, not a verdict for life. Any
time the user returns with new evidence — a recorded
demo, a second eval run, a sanitized folder, a sourced
metric — the coach re-scores from scratch.

A re-score that moves from 64 to 81 is a normal outcome
of doing the work. A re-score that does NOT move is
honest feedback that the user has not yet closed the
named gap.
```
