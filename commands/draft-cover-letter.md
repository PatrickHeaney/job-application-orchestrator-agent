# /draft-cover-letter

Run Phase 3: Draft a tailored Cover Letter structured as a strategic proposal.

## Usage
`/draft-cover-letter <folder_name>`

## Instructions
1. **Load Inputs**:
   - Read `2strategy.md` and `3resume.md` in `[ROOT]/20-user-applications/<folder_name>/`.
   - Read the master user profile from `[ROOT]/10-user-profile/user_profile.md` (or session memory/interactive input).
   - Check if `user_solutions_summary.md` exists in `10-user-profile/` and load it.
   - Check if `2research_output.md` exists in the application folder. If present, load it.
2. **Execute Drafting Prompt**:
   - Act as the **Career_Strategist** writing a strategic business proposal (tone of a confident, expert consultant).
   - Run the Cover Letter drafting prompt below. If `2research_output.md` is present, explicitly incorporate its detailed roadmap/reusable proposal ideas into the final paragraph.
3. **Save Output**:
   - Save only the generated Markdown cover letter as `4cover_letter.md` in `[ROOT]/20-user-applications/<folder_name>/4cover_letter.md`.
4. **Display to User**:
   - Render the cover letter in the chat.
   - Ask the user: *"Please review this Cover Letter proposal. Make sure it reflects your personal tone and that the achievements listed are accurate. When you are ready, say 'Proceed with audit and scoring'."*

---

## Cover Letter Drafting Core Prompt

Write a compelling, four-paragraph "Problem-Solution" cover letter.

### Narrative Blueprint

- **Header**:
  Patrick Heaney
  Durham, NC 27704 | 919.768.2422 | patrick.heaney@gmail.com | linkedin.com/in/patrickheaney

  Re: **[Job Title]** (always bold the title and any Job ID if present)

  Dear Hiring Manager,

- **Paragraph 1: The Strategic Hook (The "Why Them" & "Why You")**
  Start by addressing the Company's Strategic Initiative from `2strategy.md` (bolding the company name or the specific initiative). State the candidate's UVP as the specific solution to achieving that initiative.

- **Paragraph 2: The Differentiator (The "Strategic Bridge")**
  Use the Strategic Bridge. Take the candidate's unique, high-stakes achievement (e.g. Cisco's DoD Cloud Service or the two U.S. Army Top-10 Inventions earned by building coalitions to deliver technology under extreme ambiguity) and connect it to solving the Hiring Manager's Core Problem.

- **Paragraph 3: The Direct Fit (Hybrid Bullet Format)**
  Create a list of 3 concise, highly readable bullet points mapping directly to the strategic needs.
  - Format: Start each bullet with a **bolded metric or result** (the "Visual Hook"), followed by the context and the specific skill/tool used (e.g. "* **Boosted planning efficiency by 1200%** across 100 teams by architecting...*").

- **Paragraph 4: The Call to Value**
  State that your experience proves your ability to deliver.
  - Check if `2research_output.md` is present. If yes, extract the custom proposal framework (e.g. Sentinel-OSRE Convergence, Modernization Roadmap). If no, read `user_solutions_summary.md` and select the most relevant framework matching the core problem.
  - Propose a valuable discussion naming this framework. (e.g. *"I am eager to discuss how my **Sentinel-OSRE Convergence Framework** can be directly applied to accelerate your platform modernization and mitigate delivery risks."*)
