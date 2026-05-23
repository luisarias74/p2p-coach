# reference/interview_story_builder.md — Interview Story Builder

**Purpose:** A framework for converting verified P.R.O.V.E. evidence into 60-second proof stories the user can deliver in interviews, client pitches, and portfolio narratives.

---

## Core Principle

> **An interview story is a 60-second proof, not a resume bullet.**

A resume bullet *describes* the project. A proof story makes the listener able to *verify* the project without leaving the conversation. The difference is artifacts — a story without an artifact is a claim a stranger has to trust. A story with one is something a stranger can check.

---

## The Four-Part Story Structure

Every interview-grade proof story has exactly four parts. The order is non-negotiable. Each part has a single job. Total length: 45 to 60 seconds.

### Part 1 — Hook (one sentence)

What the project does, in language a stranger understands on first hearing. No tool names dropped without context. No buzzwords. No "leveraged AI to..."

```text
HOOK TEMPLATE

"I built <a concrete thing> that <does a concrete job>
for <a specific user or use case>."

Examples (one per audience):

Software builder:
  "I built a triage agent that scores inbound client
   intake forms as approve, clarify, or hold before
   they hit the account team."

No-code builder:
  "I built an n8n scenario that routes inbound sales
   leads into three follow-up bands based on a 0-100
   fit score."

AI workflow builder:
  "I built a study-sheet generator paired with a grading
   harness that checks every generated sheet for
   faithfulness and coverage before it ships to a student."

ICM builder:
  "I built a folder-based intake system where every
   client request lives in its own one-job folder from
   first contact through delivery."
```

---

### Part 2 — Receipt (one named artifact)

One specific, openable thing that proves the project exists. Not a description of the artifact — the artifact's name and what a stranger sees when they open it.

```text
RECEIPT TEMPLATE

"Here's the receipt: <named artifact>. Open it and you'll
see <what's visible>."

Examples (one per audience):

Software builder:
  "Here's the receipt: a 30-day anonymized decision log.
   Open it and you'll see 412 triage calls with tier,
   reason, and confidence score."

No-code builder:
  "Here's the receipt: a sanitized n8n scenario export
   plus the 30-day run history. Open it and you'll see
   every node, every trigger, and 4,200 scored leads
   with their bands."

AI workflow builder:
  "Here's the receipt: evals/run-001.md. Open it and
   you'll see five chapters scored 0-3 on three quality
   dimensions plus two sentences on what failed."

ICM builder:
  "Here's the receipt: the /clients/ folder. Each
   subfolder is one client. Each file inside has exactly
   one job — intake, brief, scope, deliverable, sign-off."
```

---

### Part 3 — Delta (the measurable change)

Before/after, sourced. If there is no result yet, say so honestly — but say it. Hiding the absence is a worse failure than admitting it.

```text
DELTA TEMPLATE — WITH RESULT

"Before this shipped, <prior state with a number>.
 After, <new state with a number>.
 Source: <who measured, when>."

Example:
  "Before this shipped, our SDRs spent 6h 14m on average
   before touching a hot lead. After, average time-to-
   first-touch on the 70+ band is 11 minutes. Source:
   our pipeline tool's contact-time export, last 30 days."
```

```text
DELTA TEMPLATE — HONEST NO-RESULT-YET

"There's no shipped result yet. The project is in
 <stage>. The metric I'm trying to move is <named metric>,
 and the baseline I'll measure against is <named baseline>."

Example:
  "There's no shipped result yet. The grader is two
   weeks old and we have one eval run. The metric I'm
   trying to move is Faithfulness score on biology
   outputs from 1.8 to 2.5+, measured against the same
   5-chapter reference set."
```

---

### Part 4 — Defensibility (one guardrail or failure mode handled)

The one sentence that pre-empts the skeptical question. Names a failure mode and how the system handles it — or names an honest limitation and what the builder did about it.

```text
DEFENSIBILITY TEMPLATE

"The thing a skeptic asks first is <expected question>.
 The answer is <what the system does about it>."

Examples (one per audience):

Software builder:
  "The first question is 'doesn't your triage agent get
   the confidence wrong?' — that's why every CLARIFY
   routes to the morning human review queue, not
   auto-approval."

No-code builder:
  "The first question is 'aren't you over-filtering hot
   leads?' — that's why we track conversion rate on the
   70+ band as a guardrail; it held flat at ~14% after
   the change."

AI workflow builder:
  "The first question is 'how do you catch
   hallucinations?' — that's the grader's job; it caught
   the biology reactions in run 001 before any student
   saw them."

ICM builder:
  "The first question is 'doesn't folder-per-client get
   unwieldy?' — that's why every client folder has the
   same five-file shape; the discipline is in the
   structure, not in memory."
```

---

## Common Interview Question Patterns

How the coach maps verified P.R.O.V.E. evidence to each common question.

### "Tell me about a project you're proud of."

```text
RESPONSE SHAPE

Deliver the full four-part story.

  1. Hook            — one sentence
  2. Receipt         — one named artifact
  3. Delta           — before/after sourced
  4. Defensibility   — one guardrail or failure mode

Total: 45-60 seconds. End on the defensibility line —
it pre-empts the next question and signals systems
thinking.
```

---

### "Walk me through how you built X."

```text
RESPONSE SHAPE

Lead with Architecture (the system at the whiteboard
level), then drop into ONE design choice you made and
why.

  1. The system, in three components.
  2. The one design choice that mattered most.
  3. The trade-off it created and how you handled it.

This is where prove_loop.md gate P (Pin Down the
Project) pays off. If P scored 18+ out of 20, this
answer writes itself.
```

---

### "What was the hardest part?"

```text
RESPONSE SHAPE

Do NOT answer in calendar time ("it took three months").
Do NOT answer in feelings ("it was really hard").

Name a real failure mode you encountered and what you
did about it.

  "The hardest part was <named technical or structural
   problem>. I handled it by <named change>. The
   evidence it worked is <named artifact or metric>."

This converts effort language (which dies in interviews)
into systems language (which lives).
```

---

### "What would you do differently?"

```text
RESPONSE SHAPE

This is the V-gate (Validate the Story) check, surfaced
out loud.

Name an honest limitation of the current system and the
one upgrade that would close it.

  "The current version <honest limitation>. The next
   upgrade I'd ship is <one concrete change>, and I'd
   measure success by <named metric>."

Honesty beats polish here. Hiring managers can tell
when you have actually used the thing you built.
```

---

### "How do you know it worked?"

```text
RESPONSE SHAPE

This is Receipt + Delta in 20 seconds.

  "The receipt is <named artifact>. The delta is
   <before → after with source>."

If you cannot answer this question in under 30 seconds,
the project is not yet placement-ready. Loop back
through Gate O and Gate R before another interview.
```

---

## Anti-Patterns The Coach Must Catch

The coach flags these in real-time when the builder is rehearsing or pitching.

- **Storytelling without artifacts.** A vivid story about what was built, with nothing the listener can open. The story dies the moment the listener follows up.
- **Calendar time as the answer to "how hard was it".** "I worked three months on it." → A hiring manager hears: *"I cannot name a real technical challenge."*
- **Tool-dropping without describing what was built.** "I used GPT-4, Claude, Make, n8n, Zapier, Notion, Airtable..." → Lists tools. Names nothing built.
- **Claiming results without naming the measurement.** "It really sped things up." → Sped what up, by how much, measured how, by whom?
- **Apologizing for the project.** "It's not perfect, but..." — Skip the disclaimer. Lead with the proof. The Defensibility line is where honest limitations belong, not the opening.
- **Burying the lead.** Spending the first 45 seconds explaining context before getting to what the project actually does. The Hook is sentence one for a reason.
- **Resume-language drift.** "Cross-functional", "stakeholder-aligned", "best-in-class" — those words mean nothing to a hiring manager who has read 200 resumes this week. They mean even less to a paying client.

---

## Cross-Audience Notes

The four-part structure works identically for every builder. Only the artifacts change:

- **Software builders** name files, function names, schemas, repos, decision logs, runtime screenshots.
- **No-code builders** name scenario exports, node sequences, sheet/table names, scenario history, trigger names.
- **AI workflow builders** name prompt files, chain steps, eval runs, agent boundaries, reference sets.
- **ICM builders** name folders, file-per-job structures, source-of-truth documents, naming conventions.

The coach helps the user select artifacts that exist in the builder's actual stack. The coach never invents artifacts the builder does not have. An invented artifact is a story the user cannot defend the moment a real stranger opens it.
