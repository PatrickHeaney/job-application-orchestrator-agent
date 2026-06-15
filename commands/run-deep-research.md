# /run-deep-research

Extract and display the custom Deep Research prompt from `2strategy.md` for execution, explaining how the output should be saved as `2research_output.md` to feed into the writing phase.

## Usage
`/run-deep-research <folder_name>`

## Instructions
1. **Read Strategy**: Open and read the `2strategy.md` file in `~/km/agentic-job-hunting/20-user-applications/<folder_name>/`.
2. **Extract Prompt**: Find the section under `## DEEP RESEARCH PROMPT`.
3. **Interactive Prompt**: Reply to the user in the chat displaying the extracted prompt in a copyable Markdown block.
4. **Display Guidelines**:
   - Provide the following instructions to the user:
     * *"Please copy the research prompt below and run it in Google Gemini (prefer Gemini Advanced with **Deep Research** enabled if available)."*
     * *"Gemini will generate a detailed, multi-phase technical proposal framework solving the company's core pain points."*
     * *"Once you get the response, save it as [2research_output.md](file:///{{USER_HOME}}/Library/Mobile%20Documents/com~apple~CloudDocs/km-icloud/agentic-job-hunting/20-user-applications/<folder_name>/2research_output.md) in the application folder (or paste it here in our chat)."*
     * *"When that's done, tell me to proceed with `/draft-resume` or `/draft-cover-letter`. I will read this research output to inject highly specific roadmaps and architectures directly into your resume summary and cover letter paragraph 4, converting your application into a high-stakes strategic proposal."*
5. **Prompt Block Format**:
   - Render the prompt clearly:
     ```
     [Extracted Deep Research Prompt text]
     ```
