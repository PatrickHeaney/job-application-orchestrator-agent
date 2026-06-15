# /calculate-score

Run Phase 5: Calculate the weighted ATS Scorecard and compile the application metadata into `8score.md` and `0overview.md`.

## Usage
`/calculate-score <folder_name>`

## Instructions
1. **Load Inputs**:
   - Read `3resume.md` and `2strategy.md` in `[ROOT]/20-user-applications/<folder_name>/`.
2. **Execute Scorecard Prompt**:
   - Embody an **ATS_Specialist**.
   - Calculate the weighted scores:
     1. Keyword Alignment (30%): Count how many of the 30 strategy keywords are in `3resume.md`. Divide by 30 and multiply by 100.
     2. Requirements Coverage (40%): Evaluate the percentage of JD qualifications addressed.
     3. Contextual Relevance (20%): Score how well the resume narrative addresses the Hiring Manager's Core Problem (1-100).
     4. ATS Formatting (10%): Score parser friendliness (100 if Markdown, 0 if images/tables are used).
   - Write `8score.md` in the application folder.
3. **Generate Overview (`0overview.md`)**:
   - Consolidate application metrics, score csv, JD URLs, company info, recruiter scan, and strategic needs into `0overview.md` in the same folder.
4. **Display to User**:
   - Render the scorecard table and final weighted score in the chat.
   - Prompt: *"Once you have reviewed your score, tell me to generate interview preparation questions using `/prep-interview <folder_name>`."*

---

## Scorecard Markdown Template (`8score.md`)

```markdown
# ATS SCORECARD

## 1. Keyword Alignment (Weight: 30%)
- **Score:** [Keyword count]/30 | [Score]%
- **Details:** List of exact matching keyword phrases found in the resume.

## 2. Requirements Coverage (Weight: 40%)
- **Score:** [Earned Qualifications]/[Total Qualifications] | [Score]%
- **Gaps:** List of critical requirements from the Strategy that are unaddressed or weak.

## 3. Contextual Relevance (Weight: 20%)
- **Score:** [Score]%
- **Justification:** Analysis of UVP narrative mapping to the Core Problem.

## 4. ATS Formatting (Weight: 10%)
- **Score:** 100%
- **Justification:** Markdown-only, single-column document parsing compatibility is verified.

---
### FINAL ATS OPTIMIZATION SCORE: [Weighted Sum]%
```

---

## Overview Markdown Template (`0overview.md`)

```markdown
# Application Overview

- **Company:** [Company Name]
- **Job Title:** [Job Title]
- **Job URL:** [Job Posting URL/Info]
- **Score CSV:** [Keyword Score], [Requirements Score], [Context Score], [Formatting Score], [Total Weighted Score]
- **Recruiter Scan Keywords:**
  1. [Keyword 1]
  2. [Keyword 2]
  3. [Keyword 3]
  4. [Keyword 4]
- **Hiring Manager Needs:**
  1. [Need 1]
  2. [Need 2]
  3. [Need 3]
- **Critical Gaps:** [Remaining unaddressed requirements]
```
