# /draft-resume

Run Phase 2: Tailor the resume to match the job posting requirements and strategic briefing.

## Usage
`/draft-resume <folder_name>`

## Instructions
1. **Load Inputs**:
   - Read `2strategy.md` in `~/km/agentic-job-hunting/20-user-applications/<folder_name>/`.
   - Read the master user profile from `~/km/agentic-job-hunting/10-user-profile/user_profile.md` (or session memory/interactive input).
   - Check if `2research_output.md` exists in the folder. If present, load and read its contents.
2. **Execute Simulation Prompt**:
   - Embody a team of two experts:
     - **ATS_Optimizer:** Focuses on 100% exact keyword phrase matching, compliance, semantic density, and single-column formatting.
     - **Career_Strategist:** Focuses on the "problem-solution" narrative, quantified stories of impact mapping to the Hiring Manager's strategic needs, and personality alignment.
   - If `2research_output.md` is present, integrate its custom technical modernization phases or frameworks into the Qualifications Summary and Career Summary to demonstrate matching expertise.
   - Run the resume tailoring prompt below.
3. **Save Output**:
   - Save only the generated Markdown resume as `3resume.md` in `~/km/agentic-job-hunting/20-user-applications/<folder_name>/3resume.md`.
4. **Display to User**:
   - Render the Qualifications Summary, Career Summary, and 5 brand subtitles to the user.
   - Ask the user: *"Please review this resume draft. Check for metric alignment, correct formatting, and verify that the bullet points represent your actual accomplishments. Once you are satisfied, tell me to proceed with the cover letter proposal."*

---

## Resume Drafting Core Prompt

Collaboratively generate an optimized resume.

### Spacing & Format Constraints
- The output MUST NOT exceed two pages when rendered.
- **Line Spacing:** Add two carriage returns (a blank line) after every line that is NOT a bullet point (starts with `-`) or a heading (starts with `#`). This applies to headers, summaries, company names, roles, and dates.
- Use only these main section titles:
  # Job Title
  # Areas of Expertise
  # Qualifications Summary
  # Professional Experience
  # Education
  # Certifications
  # Draft Subtitles

### Instructions by Section

1. **Header Details**:
   - Candidate Name: Patrick Heaney
   - Contact Info: Durham, NC 27704 | 919.768.2422 | patrick.heaney@gmail.com | linkedin.com/in/patrickheaney
   - Use the Job Title from `2strategy.md`.

2. **Career Summary**:
   - Draft a 3-sentence narrative linking candidate UVP to the Hiring Manager's Core Problem. Inject 2-3 key ATS keyword phrases naturally. Finish with a bridge statement demonstrating alignment.

3. **Areas of Expertise**:
   - Group high-value exact keywords from the strategy into 3-4 logical title-case categories. Format categories as bold followed by pipe-separated keywords.
   - *Example:* **Program Management & Strategy**: Agile Methodologies | SAFe | Stakeholder Engagement

4. **Qualifications Summary (Aggregated Achievements)**:
   - Generate 3-4 "Power Anchors" demonstrating a sustained pattern of organization-wide impact rather than one-off events.
   - Format: `- **[Thematic Title]**: [Action Verb] [Aggregated Metric/Scope] by [Strategic Approach] solving [Strategic Need].`

5. **Professional Experience**:
   - Tailor bullet points for roles in the last 15 years using the surgical formula:
     `- **[Visual Hook]**: [Narrative] [Evidence].`
   - **Visual Hook (bolded):** Start with the single most compelling quantified result ($, %, #).
   - **Narrative:** Plain text problem-solution achievement context.
   - **Evidence:** Plain text tools and exact keyword phrases used.
   - *Strict Guardrail:* Do not invent or embellish any metrics or experiences.

6. **Education & Certifications**:
   - Format Education: **University** | Degree (no bullets).
   - Format Certifications: PMI, Scrum, Cloud, and Security certifications in pipe-separated lists.

7. **Draft Subtitles**:
   - Append exactly 5 branding subtitles to the end following target structures:
     - Specialist: [Nouns] | [Nouns] | 15 Years of Experience [UVP]
     - Veteran: [Nouns] | Years of Experience in
     - Outcome Driver: [Nouns] | 15 Years of Experience [Key Outcome]
