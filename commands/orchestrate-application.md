# /orchestrate-application

Coordinate the 6-phase application optimization lifecycle interactively, pausing for human review and refinement at every milestone.

## Usage
`/orchestrate-application <folder_name>`

## Instructions
1. **Pre-flight Check**:
   - Check if `~/km/agentic-job-hunting/20-user-applications/<folder_name>/1job_posting.md` exists and contains a job description. If not, prompt the user to run `/scaffold-application <folder_name>` first.
   - Check if the master `~/km/agentic-job-hunting/10-user-profile/user_profile.md` exists. If it is missing (or if `test-mode=true` is requested), enter **Interactive Profile Mode**:
     - Prompt the user: *"I cannot find your user profile file. Please paste your master resume text or profile data here in the chat so I can parse it into session memory for this run."*
     - Wait for their input and load it as your session's Source of Truth.
2. **Execute Phase-by-Phase with Pauses**:
   - **Step 1: Strategic Analysis**: Run the logic for `/analyze-job <folder_name>`. Output `2strategy.md`. Stop and show the UVP, Core Problem, and keyword list. Ask: *"Please review this strategy. If you want any adjustments (to keywords, strategic focus, or UVP), type them here. Once you are satisfied, tell me to proceed with Deep Research."*
   - **Step 2: Deep Research Setup**: Run the logic for `/run-deep-research <folder_name>`. Present the copy-paste Gemini Deep Research prompt. Ask: *"Please run this in Gemini. Once you get the output, save it in the folder as `2research_output.md` (or paste it here in the chat). When ready, tell me to run `/draft-resume <folder_name>`."*
   - **Step 3: Resume Architecture**: Run the logic for `/draft-resume <folder_name>`. Output `3resume.md`. Pause and present the summary, anchors, and experienced bullets. Ask: *"Please review the resume draft. Let me know if we need to adjust any phrasing, bullet points, or bolding. When approved, say 'Proceed with cover letter'."*
   - **Step 4: Cover Letter Design**: Run the logic for `/draft-cover-letter <folder_name>`. Output `4cover_letter.md`. Pause and present the cover letter. Ask: *"Please review this proposal letter. Once you approve, say 'Proceed with audit and scoring'."*
   - **Step 5: Forensic Audit & Scorecard**: Run the logic for `/audit-application <folder_name>` and `/calculate-score <folder_name>`. Generate `5audit.md`, `8score.md`, and `0overview.md`. Pause and display the hallucination flag checklist and final ATS score. Ask: *"Here are the audit results. Are there any metrics we need to correct? If not, say 'Proceed to interview prep'."*
   - **Step 6: Interview Prep**: Run `/prep-interview <folder_name>`. Output `6interview_prep.md`. Present the questions and STAR answers. Ask for final edits.
   - **Step 7: Rebuild Ledger**: Run `/sync-ledger` to sync the new application, path, and score to the main `applications-ledger.md`.
3. **Persist State**:
   - Update the local `0overview.md` at the conclusion of each step.
   - Always prioritize accuracy and human feedback over speed. Never skip a pause.
