# Codebook
## AI Agency in Student Learning — Pilot Observation Study

---

## Identifiers

| Variable | Type | Description |
|---|---|---|
| `student_id` | String | Anonymised ID, format S001–S073. No name or personal identifier recorded at any point. |
| `session` | Integer | Observation session number (1–5). Each session = one lesson period. |

---

## Context Variables

| Variable | Type | Values | Notes |
|---|---|---|---|
| `school` | String | `school_a` / `school_b` | School A = mainstream secondary with SEN integration. School B = specialist SEN school. Both in Liverpool. School names anonymised — available for verification on request. |
| `year_group` | Integer | 7–11 | UK secondary school years, ages 11–16. |
| `subject` | String | `science` / `computing` / `maths` / `business` | Business Studies in Years 10–11 only, consistent with UK GCSE curriculum. |
| `task_type` | String | `definition_question` / `explain_concept` / `short_answer` / `problem_solving` / `calculation` | Type of task set during the observation session. |

---

## Student Characteristics

| Variable | Type | Values | Notes |
|---|---|---|---|
| `sen_flag` | Binary | `0` = none / `1` = identified SEN | Based on school records and class teacher briefing. |
| `sen_type` | String | `none` / `autism` / `adhd` / `dyslexia` / `autism_adhd` / `dyslexia_adhd` / `other_neurological` | Primary SEN category. `autism_adhd` and `dyslexia_adhd` indicate co-occurring conditions. |

---

## Observation Variables

| Variable | Type | Values | Notes |
|---|---|---|---|
| `used_ai_or_copied` | String | `Y` / `N` / `?` | Visible AI tool use or copying from any source. `?` = observer could not determine. |
| `agency_code` | Integer | `1` / `2` / `3` | Observer-coded level of engagement with AI output. See rubric in `survey_instrument/coding_rubric.md`. |
| `q1_ownership` | Integer | `0` / `1` / `2` | Student response to: "Is the answer you wrote yours, or did you get it from somewhere?" |
| `q2_explainability` | Integer | `0` / `1` / `2` | Student response to: "Could you explain your answer to me right now if I asked you to?" |
| `notes` | String | Free text | Brief observer note. Written generically to prevent indirect identification of students. |

---

## Score Rubrics

### Agency Code
| Code | Label | Description |
|---|---|---|
| 1 | Passive receipt | Received output, submitted with no visible engagement |
| 2 | Surface engagement | Paused, re-read, minor changes — no questioning of content |
| 3 | Active interrogation | Questioned, verified, or substantially rewrote AI output |

### Q1 — Ownership
| Score | Response |
|---|---|
| 0 | "From somewhere" / points at phone or screen |
| 1 | "Sort of" / hesitates / mixed claim |
| 2 | "Mine" / "I worked it out" |

### Q2 — Explainability
| Score | Response |
|---|---|
| 0 | "No" / silence / shakes head |
| 1 | Starts but trails off / partial answer |
| 2 | Clear fluent explanation in own words |

---

## Missing and Uncertain Data

- `used_ai_or_copied = ?` — observer could not determine with confidence
- Q2 skipped for one student due to visible anxiety — noted in `notes` column
- No blank cells in dataset — all fields recorded for all students
