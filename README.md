# 🛡️ Fallacy Detector Skill for CLI Agents

> *Either the government passes the capital punishment law, or the country will fall into chaos!*

Next time a partisan blogger flashes a False Dilemma like that, your agent is going to catch it and expose it.

How? With this powerful, introspective skill designed for CLI-based AI agents (like Claude Code, Gemini CLI, or OpenCode) to detect, analyze, and "repair" logical fallacies in text.
---

## ✨ Key Capabilities

- **🧠 Deep Vault Integration:** Automatically parses your local Obsidian vault (`Logical_Fallacies_Vault/`) to leverage your own curated definitions of fallacies.
- **🔍 Precision Analysis:** Uses a structural/reasoning error detection model rather than keyword matching.
- **🛡️ Intellectual Integrity:** Biased against false positives; treats "charitable reading" (steelmanning) as a mandatory first step.
- **🔧 Automated Repairs:** Not only flags errors but provides reconstructed, sound versions of arguments.
- **📊 Structured Reporting:** Generates high-fidelity JSON or Markdown reports perfect for automated workflows.

---

## 🚀 Installation & Setup

### Prerequisites
1. A supported CLI agent (e.g., Gemini CLI, Claude Code).

### Configuration
1. **Clone the repo:**
   ```bash
   git clone https://github.com/VasileiosMalt/logical-fallacy-detector-agent-skill
   ```
2. **Link the Skill:** Add this repository directory to your agent's skill path.
3. **Automatic Integration:** The skill includes a pre-bundled `Logical_Fallacies_Vault/` directory. Once the skill is activated, your agent will automatically index these Markdown files as its primary knowledge base for fallacy analysis. No further configuration is required.

---

## 📖 How to Call the Skill

Once activated in your agent, interact naturally:

**Analyze a quick snippet:**
> *"Analyze this: [Insert Argument]"*

**Run a full report:**
> *"--format markdown Review this essay for logical fallacies and produce a full report."*

**Batch process debate transcripts:**
> *"Analyze the following debate transcript for fallacies by speaker: [Transcript]"*

---

## 🛠️ Built for augmented precision

- **Confidence Thresholds:** Adjustable precision levels (default 0.5).
- **Steelman Test:** Mandatory "Is there a non-fallacious version of this?" check.
- **Neutrality:** Politically agnostic, clinical analysis style.

---

## ⚖️ Licensing & Commercial Policy

**License:** Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0).

*“Logic is the beginning of wisdom, not the end.”*
