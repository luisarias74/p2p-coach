# DEMO_TRANSCRIPTS.md — P2P Coach Live Sessions

## What These Transcripts Prove

P2P Coach is not a knowledge base. It is a coach. These three transcripts show it diagnosing, scoring, and rewriting three fictional projects across three different arcs:

- **Transcript 1 — From Vibe to Proof.** Full P.R.O.V.E. loop on a project with real receipts buried under vibe language. Lands at **79 / Placement Ready With Edits** with a polished Proof Rewrite.
- **Transcript 2 — The Honest Skill Gap.** A confident-sounding pitch reveals a genuine skill gap mid-conversation. Coach switches to Mentor Mode, issues an honest **38 / Critical Failure** score, and assigns a 48-hour challenge instead of a rewrite.
- **Transcript 3 — The Polish Pass.** A mostly-strong pitch enters at **72 / Placement Ready With Edits** and lands at **87 / Strong Proof Candidate** after Gate V surfaces the buried lead.

All three sessions follow the rules: one diagnostic question per coach turn, max one catchphrase per turn, the coach roasts the claim never the person, and the Proof Rewrite arrives only after diagnosis closes.

All projects are fictional. None describe a real product, company, or person.

---

---

# Transcript 1 — From Vibe to Proof

**Project:** Client Intake Triage Agent (agency operations workflow).

**Setup:** User brings in a project that has real evidence underneath it — but the opening pitch is pure vibe-code language. Coach runs the full P.R.O.V.E. loop and pulls the receipts to the surface.

---

```text
USER

"I built an AI agent for my agency to triage new client requests.
It uses GPT-4 to categorize leads as approve, clarify, or hold.
It's been a game changer for our intake process. Going to add it
to my portfolio."
```

```text
COACH — Gate P (Pin Down the Project)

EDITOR'S DESK
"Game changer" is a feeling. "AI agent" is a category. Neither
of those is a project a stranger can verify.

HEADLINE TEST
"AI agent that triages client requests" survives zero questions
from a hiring manager. There are half a million AI agents on
the internet this week.

NEXT
Name the inputs and the outputs in one sentence each.
```

```text
USER

"It takes in raw client intake form responses — name, company,
budget range, project type, timeline, free-text description —
and outputs a JSON object with a tier label (APPROVE / CLARIFY
/ HOLD), a one-line reason, and a confidence score 0-1."
```

```text
COACH — Gate P → Gate R (Reveal the Result)

EDITOR'S DESK
Good. The system has edges now. Gate P closes.

NEXT
What changed in your agency after this shipped? One before/after
number, with a source.
```

```text
USER

"Before, account leads spent about 30 minutes a day hand-sorting
the intake queue. After, they spend about 5 minutes — only on
the CLARIFY queue, because APPROVE and HOLD route automatically.
The team lead confirmed the new number in Slack on 2026-03-04."
```

```text
COACH — Gate R → Gate O (Organize the Evidence)

EDITOR'S DESK
That's a real delta — sourced, dated, defensible. Gate R closes.

RECEIPT CHECK
Numbers without artifacts are just numbers. A hiring manager
will want to open something, not just hear about it.

NEXT
Name one inspectable artifact a stranger could open without
you in the room.
```

```text
USER

"The whole decision log is in a Notion database. Every triage
call gets written there with the JSON output, timestamp, and
which account team member acted on the CLARIFY queue. There
are 412 decisions in the last 30 days."
```

```text
COACH — Gate O → Gate V (Validate the Story)

EDITOR'S DESK
Now there's something to defend. Gate O closes.

HEADLINE TEST
If I handed your portfolio entry to a stranger right now, what
is the one sentence you want them to keep?

NEXT
Write it in one line — under 25 words.
```

```text
USER

"AI triage agent that cut my agency's account-lead intake review
from 30 minutes a day to 5, by auto-routing APPROVE and HOLD
decisions and surfacing only CLARIFY for human review."
```

```text
COACH — Gate V → Gate E (Execute the Upgrade)

EDITOR'S DESK
That headline survives the first question, names the mechanism,
and reports a real delta. Gate V closes.

BURIED LEAD DETECTOR
You buried the lead in your first pitch. The morning review
queue and the confidence score were the whole story — those
are interview ammunition.

Moving to the score.
```

```text
COACH — Gate E (Score)

PLACEMENT READINESS SCORE: 79 / 100
VERDICT: PLACEMENT READY WITH EDITS

Dimension                                  Score      Notes
─────────────────────────────────────────────────────────────────────
Specificity                                18 / 20    Inputs, outputs, storage named. Decision logic slightly hand-wavy.
Proof of Shipping                          17 / 20    412 decisions, dated, in Notion. Runtime screenshot would close gap.
Outcome Clarity                            16 / 20    Sourced before/after. Add weekly volume to tighten.
Artifact Quality                           11 / 15    Notion DB real. No demo video yet — single biggest gap.
Interview Defensibility                    12 / 15    Confidence score is defensible. Low-confidence policy not named.
System / Folder Clarity (ICM alignment)     5 / 10    No public structure shown for prompts or rubric.
─────────────────────────────────────────────────────────────────────
TOTAL                                      79 / 100

GAP NARRATIVE
- Artifact Quality (11/15): The Notion DB exists but a hiring
  manager will ask "can you show me one running?" — and the
  answer needs to be one click, not "let me find it."
- System / Folder Clarity (5/10): The prompt and the tiering
  rubric live nowhere a stranger can inspect today.
```

```text
COACH — Gate E (Proof Rewrite)

ARCHITECTURE
Internal triage agent for an agency's client intake. Reads
inbound form submissions, returns a structured tier decision
(APPROVE / CLARIFY / HOLD) with a one-sentence reason and a
confidence score, then routes each decision to the appropriate
human or auto-action.

SYSTEM DESIGN
GPT-4o evaluates each form against a structured prompt; the
response is parsed into the tier JSON and written to a Notion
database. APPROVE and HOLD route through Make to the relevant
Slack channel. CLARIFY surfaces in a daily morning-review queue
the account team reads once per day.

OBSERVABLE PROOF
Account-lead intake review dropped from ~30 min/day to ~5 min/day
(source: team lead's own time tracking, confirmed in Slack
2026-03-04). 412 decisions logged in the Notion DB over the last
30 days; APPROVE and HOLD route automatically, only CLARIFY
consumes human time.

NEXT VALIDATION STEP
Record one 90-second screen capture: paste a real intake form,
show the JSON output, show the Notion row, show the Slack
handoff. Closes the Artifact Quality gap (11/15 → 15/15) and
lifts the total to ~83.
```

---

---

# Transcript 2 — The Honest Skill Gap

**Project:** Study Sheet Generator (learning app).

**Setup:** User opens confidently. Coach detects a genuine skill gap during diagnosis. Persona shifts from editor to mentor mid-conversation. No Proof Rewrite — the work is not done yet. The user leaves with a 48-hour challenge and an honest interim score.

---

```text
USER

"I built a study sheet generator using Claude. Paste in a textbook
chapter and it produces a study sheet with summary, key terms,
and practice questions. Students love it. I'm using it as my
flagship portfolio piece."
```

```text
COACH — Gate P (Pin Down the Project)

EDITOR'S DESK
"Students love it" is a feeling, not evidence. "Study sheet
generator" is a category — I can buy seven of those by lunchtime.

NEXT
Name the inputs, the outputs, and the components of your
pipeline — one sentence each.
```

```text
USER

"Input: a textbook chapter pasted as raw text. Output: a markdown
study sheet with three sections — a 3-paragraph summary, a list
of 10 key terms with definitions, and 5 practice questions.
Components: one system prompt plus one Claude call. That's it."
```

```text
COACH — Gate P → Gate R (Reveal the Result)

EDITOR'S DESK
Clean enough — the system has edges. Gate P closes.

NEXT
What changed for the people using it? One before/after, sourced.
```

```text
USER

"Students who used it scored higher on quizzes. I don't have
specific numbers — they just told me it helped."
```

```text
COACH — Gate R (held open)

EDITOR'S DESK
"Scored higher" with no number, no test, no source is not a
result. It's a testimonial wearing a metric's clothes.

That's a headline, not evidence.

NEXT
How are you checking that a generated study sheet is actually
correct — that the key terms come from the chapter, that the
questions are answerable from the chapter, that the summary
doesn't hallucinate?
```

```text
USER

"Honestly… I'm not. I read a few of them and they looked right.
I've never built validation for AI outputs before. I don't
actually know what that's supposed to look like. Is that
something I should be doing?"
```

```text
COACH — MODE SHIFT → MENTOR

EDITOR'S DESK
Yes — and asking instead of bluffing is the right move. Dropping
the volume. Switching gears.

THE GAP, IN PLAIN LANGUAGE
You have a generator. You don't have a grader. Every AI feature
that ships without a grader is shipping blind, and "how do you
know it's any good?" is the question hiring managers reach for
in the first ten minutes.

A grader answers three things about each generated sheet:

  1. Faithfulness — does the summary only contain claims that
     are actually in the source chapter?
  2. Coverage — are the key concepts from the source actually
     present in the output?
  3. Question quality — is each practice question answerable
     from the source alone?

The simplest version: a hand-curated reference set of 5 chapters
with what the ideal study sheet should contain. You run your
generator on each, score each output 0-3 on the three dimensions,
save the run as a markdown log. By hand at first. By an LLM-graded
rubric later.

This pattern is called an EVAL HARNESS (sometimes "golden set"
or "regression set"). Search "LLM eval golden dataset" — pick
one walkthrough, copy the shape.

48-HOUR CHALLENGE

  1. Pick 5 chapters across 2 subjects.
  2. Hand-write the ideal key-terms list and 3 ideal practice
     questions for each chapter.
  3. Run your generator on all 5.
  4. Score each output 0-3 on Faithfulness, Coverage, Question
     Quality.
  5. Save the whole thing as evals/run-001.md with the date,
     the scores, and 2 sentences on what failed.

That file becomes your proof artifact. Come back with it.

NEXT
Build evals/run-001.md and bring it back inside 48 hours.
```

```text
COACH — Honest Interim Score (no Proof Rewrite)

PLACEMENT READINESS SCORE: 38 / 100
VERDICT: CRITICAL FAILURE

(This is the honest score for what is on the table TODAY. It is
not a verdict on your effort. It is a verdict on the evidence.
The 48-hour challenge is designed to move this score into the
Not Placement Ready or Placement Ready With Edits range when
you return.)

Dimension                                  Score      Notes
─────────────────────────────────────────────────────────────────────
Specificity                                12 / 20    Generator described; pipeline is minimal but real.
Proof of Shipping                           8 / 20    "Students used it" but no usage records, no run logs.
Outcome Clarity                             3 / 20    Capped low: no measurable result, no source. (No Result Yet rule.)
Artifact Quality                            3 / 15    No grader file, no eval log, no inspectable sample.
Interview Defensibility                     5 / 15    Honest gap acknowledgment is a plus — but no failure mode is named yet.
System / Folder Clarity (ICM alignment)     7 / 10    A future evals/ folder would push this to full.
─────────────────────────────────────────────────────────────────────
TOTAL                                      38 / 100

NO PROOF REWRITE TODAY
A rewrite at 38 would be hype. The coach does not produce hype.

Return with evals/run-001.md and the coach re-scores from scratch.
Builders who complete this challenge honestly typically land
between 55 and 68 on the re-score — the floor for a defensible
interview story.
```

---

---

# Transcript 3 — The Polish Pass

**Project:** Lead Qualification Workflow (no-code automation in n8n).

**Setup:** User arrives with most of the proof already assembled. Initial triage score lands at 72 (Placement Ready With Edits). Coach focuses on Gate V — the buried lead — and the score moves to 87 (Strong Proof Candidate) after one polishing question.

---

```text
USER

"Built an n8n scenario for inbound lead qualification. Every
form submission gets a 0-100 score from three signals: Clearbit
company-size enrichment, OpenAI-graded ICP fit on the free-text
'about us' field, and pre-submit page-view count. Three bands —
70+ goes to SDR immediate callback, 40-69 to nurture sequence,
under 40 to newsletter only. 4,200 leads scored since November
2025. Time-to-first-touch on hot leads dropped from 6h 14m to
11 minutes."
```

```text
COACH — Initial Triage Score

EDITOR'S DESK
Strong opener. Components named, score named, bands named,
volume dated, before/after delivered.

Running the initial score before we close the remaining gaps.

PLACEMENT READINESS SCORE: 72 / 100 (initial)
VERDICT: PLACEMENT READY WITH EDITS

Dimension                                  Score      Notes
─────────────────────────────────────────────────────────────────────
Specificity                                19 / 20    Score components, bands, data sources all named.
Proof of Shipping                          17 / 20    4,200 leads dated; runtime evidence not yet shown.
Outcome Clarity                            15 / 20    Before/after named; source not stated; no guardrail mentioned.
Artifact Quality                            8 / 15    Scenario exists; no export, no screenshot, no sample runs named.
Interview Defensibility                     8 / 15    Headline survives; failure mode not named; no over-filtering check.
System / Folder Clarity (ICM alignment)     5 / 10    No folder structure shown for rubric, prompts, or runs.
─────────────────────────────────────────────────────────────────────
TOTAL                                      72 / 100

The biggest leverage point right now is Gate V. Your headline
is good — but a skeptical sales director will fire two questions
at it before they trust the metric.

NEXT
Source the time-to-first-touch number — who measured it, where
does the data come from — and name the guardrail that proves
you're not over-filtering hot leads out of the SDR queue.
```

```text
USER

"Source: our pipeline tool exports contact-time logs daily —
that's where the 6h 14m and 11 minute numbers come from, last
30 days.

Guardrail: we track conversion rate on the 70+ band as a sanity
check. It held flat at about 14% before and after the change,
so the filter isn't dropping winners."
```

```text
COACH — Gate V closes

EDITOR'S DESK
Now the headline survives both questions a sales director will
ask. Sourced. Guardrailed. Defensible.

Re-scoring.
```

```text
COACH — Gate E (Revised Score)

PLACEMENT READINESS SCORE: 87 / 100 (revised)
VERDICT: STRONG PROOF CANDIDATE

Dimension                                  Score      Notes
─────────────────────────────────────────────────────────────────────
Specificity                                19 / 20    Components, score, bands, sources all named.
Proof of Shipping                          18 / 20    4,200 leads dated; pipeline tool serves as runtime evidence.
Outcome Clarity                            19 / 20    Sourced before/after AND guardrail (conversion rate held flat).
Artifact Quality                           13 / 15    Sanitized scenario export still needed for max score.
Interview Defensibility                    13 / 15    Pre-empts "are you over-filtering?" — biggest single improvement.
System / Folder Clarity (ICM alignment)     5 / 10    No folder structure shown — the remaining weak spot.
─────────────────────────────────────────────────────────────────────
TOTAL                                      87 / 100

The conversion-rate guardrail was worth 11 points by itself.
That is the difference between a story a sales director nods
along to and a story they repeat to their VP without notes.
```

```text
COACH — Gate E (Proof Rewrite)

ARCHITECTURE
n8n scenario that scores every inbound web-form lead 0-100
using three signals (company size, ICP fit on free-text, pre-
submit engagement) and routes the lead into one of three sales-
follow-up bands — SDR immediate callback, nurture sequence, or
newsletter only.

SYSTEM DESIGN
Three signals feed the score: Clearbit enrichment (company size),
an OpenAI call (ICP-rubric grading of the free-text "about us"
field), and pre-submit page-view count from the website. The
weighted score routes through a Switch node into three downstream
branches: 70+ → Slack alert for SDR immediate callback; 40-69 →
nurture-sequence enrollment; under 40 → newsletter list.

OBSERVABLE PROOF
SDR average time-to-first-touch on 70+ leads dropped from 6h 14m
to 11 minutes (source: pipeline tool's contact-time export, last
30 days). Conversion rate on the 70+ band held flat at ~14%
across the change, confirming the filter is not over-tightening.
4,200 leads scored since November 2025; sub-40 leads no longer
consume SDR queue time.

NEXT VALIDATION STEP
Create /lead-qual/ with three files: rubric.md (ICP scoring
criteria), workflow.json (sanitized n8n export), runs/ (30
sampled scoring decisions with reasons). Closes the System /
Folder Clarity gap (5/10 → 10/10) and lifts the total to ~92 —
the range where the project is shippable to clients, not just
hiring managers.
```

---

---

## How To Read These Transcripts As A Judge

- **One coach behavior per turn.** Every coach response is doing exactly one job — running one gate, asking one question, or executing the upgrade. The coach never bundles.
- **Honest scores, not flattering ones.** Transcript 2 scores 38 because that is what the evidence supports. The coach does not soften the verdict for emotional comfort.
- **The mode switch is real, not theater.** In Transcript 2, the coach drops the editor-in-chief voice the moment the user honestly admits a gap. The 48-hour challenge replaces the rewrite. That is the persona shift boundary doing its job.
- **The polish pass is the most common arc in practice.** Most builders show up like Transcript 3 — most of the proof is there, the headline is just buried. One question from the coach moves the score 15 points.
- **No catchphrase is stacked.** Each transcript uses zero or one catchphrase per coach turn, drawn only from the approved list in identity.md. Most turns use none — catchphrases land harder when rare.
