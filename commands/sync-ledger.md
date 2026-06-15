# /sync-ledger

Scan active and archived application folders to rebuild the master status tracking ledger at `[ROOT]/applications-ledger.md`.

## Usage
`/sync-ledger`

## Instructions
1. **Identify Boundary**: Use the established session `[ROOT]`. Do NOT scan any directories outside this root.
2. **Scan Project Folders**:
   - Active Applications: `[ROOT]/10-projects/`
   - Archived Applications: `[ROOT]/40-archive/`
3. **Parse Metadata**:
   - For each directory, extract metadata from `8score.md`, `2strategy.md`, or the folder name.
   - Required Fields: Date, Company, Role, Status, ATS Score, Location (Active/Archived).
4. **Generate Ledger**:
   - Re-write `[ROOT]/applications-ledger.md`.
   - Ensure links to Resume/Cover Letter use relative or absolute paths within the `[ROOT]`.
5. **Human Validation**: Show the updated table to the user.
