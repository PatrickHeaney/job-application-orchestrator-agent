# /archive-application

Move a rejected or closed application folder to the archive directory and sync the registry.

## Usage
`/archive-application <folder_name>` (e.g. `/archive-application 2026-06-13_Agility-Robotics_TPM`)

## Instructions
1. **Verify Source**: Check if the folder `[ROOT]/20-user-applications/<folder_name>` exists.
2. **Move Folder**: Execute a shell move command to transfer the folder from `20-user-applications/` to the archive:
   - Command: `mv "[ROOT]/20-user-applications/<folder_name>" "[ROOT]/30-archived-user-applications/"`
3. **Update Status**: 
   - Open the `0overview.md` file in the newly moved folder `[ROOT]/30-archived-user-applications/<folder_name>/0overview.md`.
   - Update its `Status` field to `Archived (Rejected)` or `Archived (Closed)` based on the user's situation.
4. **Trigger Sync**: Run `/sync-ledger` to update the central tracking ledger, ensuring it lists the application's new path and status.
5. **Interactive Confirmation**: Inform the user in the chat:
   - *"I have successfully archived your application folder `<folder_name>` to the `30-archived-user-applications/` folder."*
   - *"I've also updated your master [applications-ledger.md]([ROOT]/applications-ledger.md) to reflect this status change and point to the archived path."*
