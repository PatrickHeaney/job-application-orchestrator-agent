# /prep-stakeholder

Generate a tailored preparation strategy for a specific interview panel stakeholder.

## Usage
`/prep-stakeholder <folder_name> <stakeholder_name>`

## Instructions
1. **Load Inputs & Request Stakeholder Profile**:
   - Check if the stakeholder's LinkedIn profile or biography is provided in the session.
   - If not, prompt the user in the chat: *"Please paste a LinkedIn profile summary, bio, or description of [Stakeholder Name] (e.g. their title, department, or background) so I can model their priorities."*
   - Wait for user input.
2. **Execute Stakeholder Prep Prompt**:
   - Embody a **Corporate Communications Strategist**.
   - Analyze the stakeholder's role (e.g. Engineering Manager, VP of Product, Compliance Officer) and their likely strategic interests.
   - Formulate a customized briefing detailing their priorities, how to frame the candidate's achievements (UVP) for them, and 3 high-impact questions to ask them.
3. **Save Output**:
   - Save the strategy as `6stakeholder-strategy.md` in `~/km/agentic-job-hunting/20-user-applications/<folder_name>/6stakeholder-strategy.md`.
4. **Display to User**:
   - Render the stakeholder briefing and tailored questions in the chat.

---

## Stakeholder Strategy Core Prompt

Generate the stakeholder prep guide and save it as `6stakeholder-strategy.md`. Use this exact structure:

```markdown
# STAKEHOLDER STRATEGY: [Stakeholder Name] ([Title])

## 1. Stakeholder Profile & Domain Priorities
- **Core Focus:** [What this person is responsible for and cares about most, e.g. operational efficiency, security risk, product speed-to-market]
- **Key Concerns/Risks:** [Potential concerns they might have about the candidate's experience or background]

## 2. Strategic Narrative Alignment
- **Framing the UVP:** [How the candidate should describe their value to this person]
- **Key Evidence to Cite:** [Specific achievements from the user profile to highlight during this interview, e.g. CISCO DoD Cloud certification for a Security Auditor]

## 3. High-Impact Questions to Ask
1. [Question 1: Positioned to demonstrate industry intelligence and address their specific domain]
2. [Question 2]
3. [Question 3]
```
