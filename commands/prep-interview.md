# /prep-interview

Run Phase 6: Generate behavioral and situational interview questions with tailored STAR/IM-PACT speaker notes.

## Usage
`/prep-interview <folder_name>`

## Instructions
1. **Load Inputs**:
   - Read `1job_posting.md`, `2strategy.md`, and `3resume.md` in `~/km/agentic-job-hunting/20-user-applications/<folder_name>/`.
   - Read the master user profile from `~/km/agentic-job-hunting/10-user-profile/user_profile.md` (or session memory/interactive input).
2. **Execute Interview Prep Prompt**:
   - Embody an **Executive Interview Coach**.
   - Generate "Tell me about yourself" + 9 situational/strategic questions directly linked to the Hiring Manager's Strategic Needs.
   - For each question, draft a response using the appropriate model (STAR for tactical, IM-PACT for program leadership, PARLA for retrospectives).
   - Use a short **telegraphic speaker notes** style (notes, not full quotes). Include hard metrics in each answer and end by tying back to the JD requirements.
3. **Save Output**:
   - Save the prep guide as `6interview_prep.md` in `~/km/agentic-job-hunting/20-user-applications/<folder_name>/6interview_prep.md`.
4. **Display to User**:
   - Render the opening question and first two STAR notes in the chat.
   - Inform the user: *"Your full interview prep guide is ready in 6interview_prep.md. You can also run `/prep-stakeholder <folder_name> <stakeholder_name>` to prepare tailored messaging for specific panel interviewers."*

---

## Interview Prep Core Prompt

Generate the interview prep notes and save them as `6interview_prep.md`. Use this exact structure:

```markdown
# INTERVIEW PREPARATION NOTES

## Question 1: Tell me about yourself.
- **Response Model:** IM-PACT
- **Speaker Notes:**
  - *Intention:* [Why you do what you do]
  - *Method:* [Your framework summary]
  - *Proof:* [High-level career metric, e.g. Cisco/Army inventions]
  - *Action:* [Recent impact]
  - *Connect:* [Tie-back to this role]

## Question 2: [Strategic Question 1]
- **Response Model:** [STAR / IM-PACT / PARLA]
- **Speaker Notes:**
  - *Situation/Intention:* [Context]
  - *Task/Method:* [What needed to be done]
  - *Action:* [Specific engineering/program step]
  - *Result/Proof:* [Quantified outcome]
  - *Connect/Learning:* [Direct alignment to requirements]

[Repeat for remaining 8 questions]
```
