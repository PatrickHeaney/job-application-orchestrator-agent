# PM Career Agent Plugin (Open Source)

The `pm-career` agent plugin is a high-fidelity, modular capability designed to automate and optimize the job application value stream. It integrates a **Career Conductor** agent with specialized sub-skills for analysis, resume tailoring, and deep research.

---

## 🚀 Key Features
- **Sovereignty-First**: Operates within your designated local workspace. No personal data leaks.
- **Momentum Architecture**: Uses the "Agentic Data Bus" framework to compress cycle times.
- **ATS Optimization**: Forensic auditing against job descriptions for maximum match scores.
- **Multi-Phase Workflow**: Guided 9-step lifecycle from lead discovery to interview prep.

## 📂 Structure
- `agents/`: The `Career-Conductor` identity and operational mandates.
- `skills/`: Modular logic for Analyst, Writer, Auditor, and Deep Research.
- `commands/`: User-centric slash commands (e.g., `/set-root`, `/new-application`).
- `mcp/`: Configuration for Gmail and other tool integrations.

## 🛠️ Installation & Setup
1. **Link the Plugin**: Add the absolute path to this folder to your agent platform (e.g., Gemini CLI or VS Code).
2. **Initialize Workspace**: Run `/set-root` to establish your sovereignty boundary.
3. **Set Your Profile**: Copy `10-user-profile/user_profile.template.md` to `user_profile.md` and populate your data.

## 🤝 Contributing
This is an open-source project. We welcome contributions to:
- **Prompt Engineering**: Refining the `2strategy.md` generation logic.
- **New Skills**: Adding specialized capabilities for portfolio mapping or technical interviews.
- **UX Improvements**: Improving command feedback and help documentation.

## ⚖️ License
Distributed under the **MIT License**. See `LICENSE` for details.
