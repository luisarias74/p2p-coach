# P2P Coach — Proof-to-Placement Coach

> **Projects don't get you hired. Proof does.**

P2P Coach is a folder-based AI coach that turns vague project claims into hireable proof, interview-ready stories, and portfolio evidence sharp enough for a stranger to understand in 60 seconds.

Drop the folder into a Claude project. Claude becomes the coach.

---

## The 30-Second Demo

**Before — what most people pitch:**

```text
I built an awesome AI onboarding workflow for an agency client. It reads incoming client emails and totally streamlines everything by deciding if we should work with them or not. It saves the team tons of time and makes everything way smoother.
```

**The coach's response:**

```text
[Editor's Desk]
You buried the lead. "Streamlines everything" is a marketing brochure headline, and a hiring manager is not a mind reader. I do not care about "awesome workflows" until I can see the artifact.

Receipt Check: What exact folder, file, or automation node processes incoming client text and assigns APPROVE, CLARIFY, or HOLD?
```

**After the coaching cycle closes — placement-ready proof:**

```text
Built a Client Intake Triage Agent inside an agency-triage/ workflow that processes incoming client emails through scripts/evaluate_lead.py and applies config/triage_rules.json to classify each lead as APPROVE, CLARIFY, or HOLD.

The system reduces subjective first-pass filtering by routing incoming lead records through the same defined classification path before CRM insertion. Next validation step: run 50 historical intake logs through the workflow and document classification accuracy, misroutes, and edge cases.

Placement Readiness Score: 79 / 100 (Placement Ready With Edits)
```

That's the entire product. The coach does this for any project the user brings.

---

## What This Is

A folder of markdown files. When you drop it into a Claude project, Claude reads the files and becomes the P2P Coach — a newsroom-editor-style coach that:

- Diagnoses before rewriting
- Forces evidence before accepting claims
- Scores readiness honestly (no inflation)
- Switches to mentor mode when it detects a real skill gap
- Roasts the claim, never the person

The coach is *not* a knowledge base. A knowledge base answers questions. A coach asks them.

---

## Who It's For

- **AI builders** shipping prompt chains, agents, and LLM-powered workflows
- **No-code builders** working in Zapier, Make, n8n
- **Freelancers** turning client work into pitchable proof
- **Implementation learners** building folder-based ICM-style systems
- **Anyone** who has projects but can't explain them as evidence

---

## How to Use

1. Clone or download this repo
2. Add the folder contents to a Claude project
3. Start a conversation: *"Coach me on [your project]"*
4. Answer one diagnostic question per turn until the coach issues a Proof Readiness Score and Proof Rewrite

---

## The P.R.O.V.E. Loop

The coach runs every project through five sequential gates:

```text
P — Pin Down the Project       What did you build? Name the components.
R — Reveal the Result          What changed? Show the before/after.
O — Organize the Evidence      What artifact can a stranger open?
V — Validate the Story         Does the headline survive one tough question?
E — Execute the Upgrade        Score, gap analysis, polished rewrite.
```

One gate at a time. One question per turn. The coach never advances on charm.

---

## The Proof Readiness Score

Every evaluated project gets a score out of 100 across six dimensions:

| Dimension | Points |
|---|---|
| Specificity | 20 |
| Proof of Shipping | 20 |
| Outcome Clarity | 20 |
| Artifact Quality | 15 |
| Interview Defensibility | 15 |
| System / Folder Clarity (ICM alignment) | 10 |

**Verdict gates:**

- **0–49** — Critical Failure
- **50–69** — Not Placement Ready
- **70–84** — Placement Ready With Edits
- **85–100** — Strong Proof Candidate

The coach shows the breakdown for every score. A number without a breakdown is a verdict without a diagnosis.

---

## What's In This Folder

| File | Purpose |
|---|---|
| `identity.md` | The coach's persona and voice rules |
| `rules.md` | Coaching rules, MUST/MUST NOT, Persona Shift Boundary |
| `examples.md` | Three weak-to-strong project rewrites |
| `DEMO_TRANSCRIPTS.md` | Three complete coaching conversations |
| `reference/prove_loop.md` | The 5-gate operating manual |
| `reference/weak_project_detector.md` | Fluff-phrase taxonomy with pushbacks |
| `reference/readiness_scorecard.md` | The 100-point rubric and scoring honesty rules |
| `reference/interview_story_builder.md` | Turning proof into 60-second interview stories |
| `reference/proof_rewrite_template.md` | The Architecture/System Design/Observable Proof format |
| `JUDGE_GUIDE.md` | 5-minute walkthrough for competition judges |
| `QUICK_TEST.md` | Copy-paste prompts to test the coach immediately |

---

## For Judges

Start here:

1. **DEMO_TRANSCRIPTS.md** — proves the coach actually coaches
2. **QUICK_TEST.md** — copy-paste prompts you can run in your own Claude
3. **JUDGE_GUIDE.md** — 5-minute walkthrough with the judging criteria mapped

---

## License

MIT.

---

*Built for Clief Notes Weekly Competition #5: The Coach.*