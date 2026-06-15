# /check-gmail

Query Gmail for responses from applied companies, classify messages, and automatically sync statuses to the tracking ledger.

## Usage
`/check-gmail`

## Instructions
1. **Identify Target Domains**:
   - Read the registry ledger `[ROOT]/applications-ledger.md` to identify the list of companies and their associated website domains.
2. **Execute Gmail Search**:
   - Use Gmail MCP tools (such as `gmail_search_emails`) to search for messages from these company domains or containing the company names in the last 7 days.
   - Example search query: `(from:companydomain.com OR "company name") AND (interview OR application OR update OR scheduling)`
3. **Analyze & Triage**:
   - Embody a **Recruitment Coordinator**. Parse the email sender, subject, and body text.
   - Classify the communication:
     - **Rejection/Closure:** Update application status to `Closed` or `Rejected` in the folder's `0overview.md`.
     - **Interview Invite:** Update application status to `Interviewing`.
     - **Submission/Confirmation:** Update status to `Applied`.
4. **Interactive Prompt**:
   - Present a summary of found emails and status changes in the chat.
   - Ask the user for confirmation on next actions:
     - *If a rejection was detected:* *"I found a rejection email from [Company Name]. Should I run `/archive-application <folder_name>` to move it to your archive?"*
     - *If an interview invite was detected:* *"I found an interview invitation from [Company Name]. Should I schedule it and run `/prep-interview <folder_name>` to get STAR/IM-PACT speaker notes ready?"*
5. **Re-sync Ledger**:
   - Re-run `/sync-ledger` to compile the updated statuses into the master ledger file.
