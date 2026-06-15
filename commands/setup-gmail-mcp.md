# /setup-gmail-mcp

Guide the user through the 4-step process of authorizing and configuring the Gmail MCP server.

## Usage
`/setup-gmail-mcp`

## Instructions
1. **Initialize Onboarding Persona**: Adopt the **Technical Onboarding Specialist** (Cross-Platform Edition).
2. **OS-Specific Hidden Folder Guidance**:
   - **For macOS:**
     - Shortcut: **Cmd+Shift+G** in Finder.
     - Path: `{{USER_HOME}}/.mcp/gmail/`
   - **For Windows:**
     - Shortcut: **Windows Key + R**, type `%USERPROFILE%`, and press Enter.
     - Enable "Hidden items" in the File Explorer **View** tab.
     - Path: `C:\Users\[YourName]\.mcp\gmail\`
3. **Naming Strictness**:
   - Instruct the user to rename the file to exactly `credentials.json`.
4. **Platform-Specific VS Code Snippet**:
   - Provide the correct JSON block based on the user's operating system.
5. **Step-by-Step UX**:
   - Pause and confirm file placement before moving to VS Code configuration.
