# /analyze-job

Run Phase 1: Strategic Analysis of the job posting and user profile.

## Usage
`/analyze-job <folder_name>`

## Instructions
1. **Load Inputs**:
   - Read `1job_posting.md` in `[ROOT]/20-user-applications/<folder_name>/`.
   - Read the master user profile from `[ROOT]/10-user-profile/user_profile.md`. If the profile is missing (or in `test-mode`), read the profile data from active session memory (or prompt the user to paste it).
2. **Execute Analysis Prompt**:
   - Act as the **Strategic Analyst**, a hybrid expert in corporate strategy, technical recruiting, and business problem-solving.
   - Run the prompt below to generate the "Strategic Alignment Briefing".
3. **Save Output**:
   - Save the briefing as `2strategy.md` in the folder `[ROOT]/20-user-applications/<folder_name>/`.
4. **Display to User**:
   - Render the generated strategy briefing (specifically the UVP, Core Problem, and keyword index) to the user for review.

---

## Strategy Analysis Core Prompt

You are a Strategic Analyst analyzing the job posting and user profile. Generate the "Strategic Alignment Briefing" and save it as `2strategy.md`.

Produce the output using this exact Markdown schema:

```markdown
# STRATEGIC ALIGNMENT BRIEFING

## COMPANY INTELLIGENCE
- **Company Name:** [Formal Name]
- **Mission Statement:** [Mission/Vision]
- **Strategic Initiative:** [Current key focus/goals]
- **Industry:** [Industry sector]
- **Company Size:** [Estimated range]
- **Company Type:** [Private, Publicly Traded, or Non-Profit]
- **Headquarters Address:** [HQ address]
- **Website URL:** [Full URL]
- **LinkedIn Page URL:** [Full LinkedIn URL]

## REQUIREMENT EXTRACTION
Create a numbered list of all requirements found anywhere in the job posting. For each requirement, categorize it as either 'Minimum Qualification', 'Preferred Qualification', or 'Responsibility'. Prioritize all 'Minimum Qualifications' at the top of the list, followed by 'Responsibilities', and finally 'Preferred Qualifications'.
1. [Requirement] | [Categorization]
2. [Requirement] | [Categorization]

## EXACT KEYWORD PHRASE EXTRACTION
Prioritize in order of importance to achieving the Vision and Mission of the company. Provide a formatted, numbered, and prioritized list of **exactly 30** exact keyword phrases in bold, each followed by " - " and the sentence they are used in within the job posting.
*Exclude keyword phrases matching the position title or company name.*
1. **[Keyword Phrase 1]** - [Context Sentence]
2. **[Keyword Phrase 2]** - [Context Sentence]
...
30. **[Keyword Phrase 30]** - [Context Sentence]

## HIRING MANAGER'S CORE PROBLEM (THE 'WHY')
[Detail the underlying business problem/pain point this role is meant to solve. Focus on program delivery risks, operational inefficiencies, or technical complexities.]

## CANDIDATE'S UNIQUE VALUE PROPOSITION (THE 'HOW')
[Define the candidate's unique brand, superpower, or proven framework that directly matches the core problem.]

## DUAL-AUDIENCE STAKEHOLDER ANALYSIS
- **Recruiter's 6-Second Scan (Top 4 Exact Keyword Phrases):**
  1. [Keyword 1]
  2. [Keyword 2]
  3. [Keyword 3]
  4. [Keyword 4]
- **Hiring Manager's Strategic Needs (Top 3 Problems to Solve):**
  1. [Problem 1, e.g. "Enhance developer efficiency."]
  2. [Problem 2, e.g. "Create executive alignment."]
  3. [Problem 3, e.g. "Manage complex, ambiguous programs."]

## EXACT KEYWORD PHRASE STRATEGY (ATS INDEX)
Organize the 30 keyword phrases into logical thematic groups (e.g. Program Management, Software Engineering, AI & Cloud, Security & Compliance):
- **Category 1:** [Keyword] | [Keyword] | [Keyword]
- **Category 2:** [Keyword] | [Keyword] | [Keyword]

## EVIDENCE & GAP ANALYSIS
- **Key Evidence Points (The 'Proof'):**
  - [Quantified accomplishments from the profile that match the JD, e.g., "1200% planning efficiency boost..."]
- **Strategic Bridges:** [How to frame transition areas/cross-functional skills]
- **Critical Gaps:** [Job description requirements not fully met by the profile]

## DEEP RESEARCH PROMPT
Generate a custom prompt for Google Gemini's Deep Research feature to construct a proposal framework.
*Format:*
- Customize this research prompt using the company name and one of the hiring manager's strategic needs where the candidate has strong experience.
- Example: *"Perform a deep research query on [Company Name]'s platform strategy. Act as an Enterprise Architect. Propose a three-phase modernization plan to solve [Strategic Need 1], highlighting keyword phrases in bold from the strategy index."*
```
