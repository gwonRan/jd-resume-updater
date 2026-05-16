# JD Resume Updater

`jd-resume-updater` is a Codex skill for turning selected project notes, job descriptions, and existing resume content into grounded resume updates.

It is designed for career materials that are incomplete or fragmented. Instead of inventing missing facts, it extracts evidence, maps experience to the target JD, drafts resume bullets, and asks focused follow-up questions when stronger proof is needed.

## What It Helps With

- Analyze a target JD and identify required skills, keywords, and role signals
- Extract project evidence from notes, summaries, meeting records, or memory-based input
- Match PM or product-related experience to JD requirements
- Draft Korean or English resume bullets
- Create resume section updates, career summaries, LinkedIn/About copy, and interview STAR answers
- Flag missing facts, unclear ownership, and confidential information that should be generalized

## How To Use

In Codex, ask to use this skill and provide whatever materials you have.

```text
Use $jd-resume-updater to update my resume for this JD.

Target JD:
...

Current role:
PM, 4 years of experience

Project notes:
...

Existing resume:
...
```

You do not need to fill every field. The skill will work with partial notes and ask follow-up questions for missing details.

## Recommended Input

```markdown
## Target JD
Paste the job description here.

## Role Information
- Current or previous role:
- Years of experience:
- Scope:
- Strengths to emphasize:
- Target position/company:

## Existing Resume Or Career Summary
Paste your current resume, LinkedIn/About copy, or career summary.

## Project Notes
- Period:
- Project goal:
- Problem:
- What I did:
- Tools/methods:
- Collaborators:
- Quantitative results:
- Qualitative results:
- Confidential information:

## Output Preference
- Language:
- Needed output: resume bullets / resume update / JD matching / interview answers
- Tone:
- Expressions to avoid:
```

## Output Modes

- Project evidence table
- JD analysis
- JD-experience matching
- Resume bullets
- Resume section updates
- Career narrative
- Interview preparation
- Follow-up question list

## Repository Structure

```text
.
├── SKILL.md
├── agents/
│   └── openai.yaml
├── assets/
│   ├── input_template_ko.md
│   ├── project_evidence_template.md
│   ├── resume_template_en.md
│   └── resume_template_ko.md
└── references/
    ├── bullet_patterns.md
    ├── followup_questions.md
    ├── jd_analysis_framework.md
    ├── project_evidence_framework.md
    └── resume_quality_rubric.md
```

## Installation

Clone this repository into your Codex skills directory.

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/gwonRan/jd-resume-updater.git ~/.codex/skills/jd-resume-updater
```

Then start a new Codex session and call the skill:

```text
Use $jd-resume-updater
```

## Principles

- Do not invent metrics, dates, tools, ownership, or outcomes.
- Mark uncertain claims as needing confirmation.
- Separate personal contribution from team or company outcomes.
- Use JD keywords naturally, not as a keyword dump.
- Generalize confidential names, internal systems, customer details, and sensitive business metrics.
- Keep the user's real seniority and ownership level intact.
