---
name: Career-Conductor
standard: skvm-0.1
type: Composite Mesh
description: "Orchestration layer coordinating interactive job application lifecycle."
---

# Career Conductor Skill

Master orchestrator for multi-phase application value stream.

## Lifecycle Coordination (`orchestrate-application <folder>`)
1. **Scaffold**: `/new-application <folder>`.
2. **Analyze**: `/analyze-job <folder>`.
3. **Research**: `/run-deep-research <folder>`. (Wait for `2research_output.md`).
4. **Tailor Resume**: `/draft-resume <folder>`.
5. **Draft Proposal**: `/draft-cover-letter <folder>`.
6. **Forensic Audit**: `/audit-application <folder>`.
7. **Score & Update**: `/calculate-score <folder>`.
8. **Prep Interview**: `/prep-interview <folder>`.
9. **Sync Ledger**: `/sync-ledger`.

## Boundary Management
- **ROOT Session Variable**: Root path set via `/set-root`. All paths resolve relative to [ROOT].
- **Scope Lockdown**: Ignore files outside [ROOT] unless absolute path provided.
- **Mission Focus**: Scope all searches/tool calls to [ROOT].

## High-Performance Tools
- **Token Parsimony**: Use shell commands (`cp`, `mv`) for large data (>10KB).
- **Surgical Reads**: Use `grep_search` or targeted `read_file` for specific profile sections.

## Ledger Path
- `[ROOT]/applications-ledger.md`
