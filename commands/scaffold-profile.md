# /scaffold-profile

Detect, template, and interactively import or interview the user to build the source of truth profile at `[ROOT]/10-user-profile/user_profile.md`.

## Instructions
1. **Check Path**: Check if `[ROOT]/10-user-profile/user_profile.md` exists.
2. **If Already Exists**:
   - Inform the user that their user profile already exists.
   - Ask: *"Would you like to review/edit the profile, or would you like to run a test-mode interactive load for this session?"*
3. **If Missing**:
   - Create the directory `[ROOT]/10-user-profile/`.
   - Write the empty structured template below to `user_profile.md`.
   - Ask the user in chat: *"I've scaffolded your profile at 10-user-profile/user_profile.md. Do you have an existing resume you'd like me to import, or would you like to do a quick step-by-step interview to fill it out?"*
4. **Collect & Format**:
   - If they paste their resume, parse it into the template structure and save the results to the file.
   - If they choose the interview, ask them:
     1. Contact details.
     2. Target job titles and core expertise (UVP).
     3. 3-4 key accomplishments with metrics (e.g. revenue saved, cycle times improved).
     4. Recent company experience, roles, dates, and bullet points.
     5. Education & top certifications.
   - Compile their responses, format them nicely, and overwrite the file.

---

## User Profile Markdown Schema Template
```markdown
# User Profile (Source of Truth)

## Contact Information
- Name: 
- Location: 
- Phone: 
- Email: 
- LinkedIn: 

## Core Achievements & Unique Value Proposition (UVP)
- **UVP:** [2-sentence statement of your unique brand/value]
- Key Achievement 1: [Quantified metric + action + scale]
- Key Achievement 2: [Quantified metric + action + scale]
- Key Achievement 3: [Quantified metric + action + scale]

## Professional Experience
### [Company Name]
- **Role:** [Job Title]
- **Dates:** [Start Date] - [End Date/Present]
- **Key Metrics/Outcomes:**
  - [e.g. Saved $10M/year by...]
  - [e.g. Scaled platform to 10M users...]
- **Responsibilities & Achievements:**
  - [Detail achievement bullet 1]
  - [Detail achievement bullet 2]
- **Tech Stack & Tools:** [e.g. Generative AI, Python, JIRA]

## Education
- **[University Name]** | [Degree, Major/Focus] ([Graduation Year])

## Certifications & Training
- [Certification Name] ([Issuing Org], [Year])
```
