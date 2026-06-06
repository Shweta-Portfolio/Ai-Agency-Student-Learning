# AI Agency in Student Learning
### A Pilot Observation Study — Secondary Schools, Liverpool, UK (2026)

**Shweta Debjit Sarkar** | Teaching Assistant & Independent Researcher  
`shweta.sarkar.academic@gmail.com` | [LinkedIn](https://linkedin.com/in/shwetapooja) | [GitHub](https://github.com/Shweta-Portfolio)

---

## The Question

When a student receives an AI-generated answer, do they act as the **agent checking it** — or as the **recipient of it**?

Two students can submit identical correct answers: one interrogated the AI output, questioned it, and rewrote it in their own words. The other copied it without engagement. Their grades look the same. Their understanding is not.

Current assessment methods cannot see this difference. This study attempts to make it visible.

---

## Why This Matters

AI tools can now produce correct-looking answers to the kinds of tasks engineering and science students are routinely assessed on. This creates a structural problem: the gap between *producing an answer* and *understanding the reasoning behind it* has never been easier to hide — and existing assessment frameworks were not designed to detect it.

This pilot study is grounded in direct classroom experience as a teaching assistant across two secondary schools in Liverpool, including a specialist environment for students with neurological and developmental needs. That population makes the distinction between procedural task completion and genuine conceptual ownership especially visible — which is what makes this setting valuable for studying the question.

---

## Study Design

### Participants
- **N = 73 students**, Years 7–11 (ages 11–16)
- **2 schools in Liverpool:**
  - School A — mainstream secondary school with integrated SEN provision
  - School B — specialist school for students with neurological and developmental needs
- **53% identified SEN** across six categories: autism, ADHD, dyslexia, autism+ADHD, dyslexia+ADHD, other neurological
- **5 observation sessions** across Science, Computing, Maths, and Business Studies (Years 10–11 only)

*School names are anonymised. Real institutional identifiers available on request for verification.*

### Procedure

**Step 1 — Task (10 minutes)**
Students complete a short subject task using any resources available — AI tools, internet, textbook, peers. No instruction about AI use is given. The goal is to observe natural behaviour.

**Step 2 — Observation (during task)**
The observer records three things per student:
- Did the student use an AI tool or copy from a screen?
- After receiving AI output, did they do anything with it before writing?
- What did that behaviour look like? (brief observer note)

**Step 3 — Two follow-up questions (2 minutes)**
Asked verbally immediately after the task, or shown on a printed card for students who prefer pointing over speaking:

> **Q1:** *"Is the answer you wrote yours, or did you get it from somewhere?"*
> **Q2:** *"Could you explain your answer to me right now if I asked you to?"*

Responses coded 0–2. Non-verbal responses accepted via printed card.

---

## Variables

| Variable | Description | Values |
|---|---|---|
| `student_id` | Anonymised ID | S001–S073 |
| `session` | Observation session | 1–5 |
| `school` | School identifier | school_a / school_b |
| `year_group` | UK school year | 7–11 |
| `subject` | Subject observed | science / computing / maths / business* |
| `task_type` | Type of task | definition_question / explain_concept / short_answer / problem_solving / calculation |
| `sen_flag` | Identified SEN | 0 = none / 1 = yes |
| `sen_type` | SEN category | none / autism / adhd / dyslexia / autism_adhd / dyslexia_adhd / other_neurological |
| `used_ai_or_copied` | Visible AI use | Y / N / ? |
| `agency_code` | Engagement level | 1 / 2 / 3 |
| `q1_ownership` | Ownership response | 0 / 1 / 2 |
| `q2_explainability` | Explainability response | 0 / 1 / 2 |
| `notes` | Observer note | Free text |

*Business Studies in Years 10–11 only, consistent with UK GCSE curriculum structure.

---

## Coding Rubric

### Agency Code

| Code | Label | What it looks like |
|---|---|---|
| **1** | Passive receipt | Receives AI output, submits without visible engagement |
| **2** | Surface engagement | Pauses, re-reads, minor changes — no questioning of content |
| **3** | Active interrogation | Asks "is this right?", checks another source, rewrites in own words, spots an error |

### Q1 — Ownership

| Score | Response |
|---|---|
| 0 | "Got it from somewhere" / points at phone |
| 1 | "Sort of" / hesitates / "I changed some of it" |
| 2 | "Mine" / "I worked it out" |

### Q2 — Explainability

| Score | Response |
|---|---|
| 0 | "No" / silence / shakes head |
| 1 | Starts but trails off / partial answer |
| 2 | Clear explanation in own words |

---

## Key Findings

### 1. Most students showed passive or surface-level AI engagement

| Agency Level | N | % |
|---|---|---|
| Code 1 — Passive receipt | 34 | 47% |
| Code 2 — Surface engagement | 24 | 33% |
| Code 3 — Active interrogation | 15 | 21% |

### 2. Active interrogation predicts explainability

Students who actively interrogated AI output (Code 3) showed substantially higher mean explainability scores than passive students (Code 1). The relationship is consistent across all three agency levels.

| Agency Code | Mean Explainability (Q2) |
|---|---|
| Code 1 | 0.47 |
| Code 2 | 0.96 |
| Code 3 | 1.73 |

### 3. The mismatch finding

**32% of students claimed the answer was theirs (Q1 = 2) but could not explain it (Q2 ≤ 1).**

These students were predominantly in the passive receipt group. This is the study's most significant preliminary finding: students may not recognise the gap between *having* an answer and *understanding* it. They are not being dishonest — they genuinely believe the answer is theirs. This gap is invisible to current assessment methods.

### 4. Patterns hold across SEN and non-SEN populations

The agency distribution and mismatch pattern appear in both SEN and non-SEN subgroups. SEN students do not show systematically lower agency scores.

---

## Limitations

- N = 73 is sufficient for descriptive analysis but too small for statistical inference
- Single observer — a second coder would be needed for reliability assessment
- Naturalistic observation — AI use was not controlled or standardised
- Self-report responses may be affected by social desirability
- No formal ethics review — naturalistic observation within normal teaching duties
- Results should not be generalised beyond this setting without replication

---

## Repository Structure

```
README.md
LICENSE
CONTRIBUTING.md
data/
  observations_anonymised.csv    ← Full dataset (N=73)
  codebook.md                    ← Variable definitions
survey_instrument/
  observation_sheet.md           ← Observer recording sheet
  student_questions_card.md      ← Printed card for students
  coding_rubric.md               ← Full rubric with examples
notebook/
  analysis.ipynb                 ← Full analysis (Google Colab)
figures/
  agency_distribution.png
  agency_by_year.png
  mismatch_analysis.png
  agency_vs_scores.png
  sen_analysis.png
  subject_comparison.png
```

---

## Ethical Considerations

- No student names recorded at any point — numeric IDs only
- School names anonymised — available for verification on request
- Observation task is normal classroom activity — no additional burden on students
- Follow-up questions are conversational and optional
- Students who appeared anxious had Q2 skipped
- Non-verbal students used a printed pointing card
- No formal IRB review — non-interventional naturalistic study. Any scaled version would require full ethics approval.

---

## Connection to Doctoral Research

This pilot study directly informs a research interest in engineering education at the intersection of AI, student agency, and assessment design — specifically whether assessment formats can be redesigned to make student reasoning visible rather than just final outputs.

It forms part of an application to the PhD position *"Rethinking Electrical Engineering Education in the Age of AI"* at TU Delft's Electrical Engineering Education section (Faculty of EEMCS).

---

## How to Reproduce

1. Open [Google Colab](https://colab.research.google.com)
2. Open `notebook/analysis.ipynb`
3. Run cells top to bottom — data is embedded, no file uploads needed

---

## Citation

> Sarkar, S.D. (2026). *AI Agency in Student Learning: A Pilot Observation Study*. Independent research, Liverpool, UK. https://github.com/Shweta-Portfolio/ai-agency-student-learning

