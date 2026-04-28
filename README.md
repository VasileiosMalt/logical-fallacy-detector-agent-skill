# <p align="center"> Logical Fallacy Detector Agent Skill </p>

<p align="center">
  <img src="https://raw.githubusercontent.com/VasileiosMalt/logical-fallacy-detector-agent-skill/refs/heads/main/LF_skill_image.png" width="300"/>
</p>

> *Either the government passes the capital punishment law, or the country will fall into chaos!*

Next time a partisan blogger flashes a False Dilemma like that, your agent is going to catch it and expose it.

How? With this powerful, introspective skill designed for CLI-based AI agents (like Claude Code, Gemini CLI, or OpenCode) to detect, analyze, and "repair" logical fallacies in text.

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![Agent Skill](https://img.shields.io/badge/Agent-Skill-blueviolet)](https://github.com/VasileiosMalt/logical-fallacy-detector-agent-skill)
[![Supports: Claude Code](https://img.shields.io/badge/Supports-Claude%20Code-orange)](https://github.com/anthropics/claude-code)
[![Supports: Gemini CLI](https://img.shields.io/badge/Supports-Gemini%20CLI-blue)](https://github.com/google-gemini/gemini-cli)

---

# ✨ Key Capabilities

| Feature | Description |
|---|---|
| 🧠 **Deep Vault Integration** | Parses your local `Logical_Fallacies_Vault/` (Obsidian-compatible) to use your own curated fallacy definitions |
| 🔍 **Precision Analysis** | Detects structural and reasoning errors — not just keyword matches |
| 🛡️ **Intellectual Integrity** | Steelmanning is a mandatory first step; biased heavily against false positives |
| 🔧 **Automated Repairs** | Doesn't just flag errors — reconstructs sound, corrected versions of arguments |
| 📊 **Structured Reporting** | Outputs clean JSON or Markdown reports, ready for automated pipelines |
| 🎚️ **Confidence Thresholds** | Adjustable precision levels (default: `0.5`) |

---

## 🚀 Installation & Setup

### Prerequisites

- A supported CLI agent: [Gemini CLI](https://github.com/google-gemini/gemini-cli), [Claude Code](https://github.com/anthropics/claude-code), or [OpenCode](https://github.com/sst/opencode)

### Steps

**1. Clone the repository:**
```bash
git clone https://github.com/VasileiosMalt/logical-fallacy-detector-agent-skill
cd logical-fallacy-detector-agent-skill
```

**2. Link the skill to your agent:**

Add the cloned directory to your agent's skill/tool path. For example, in **Gemini CLI**:
```bash
export GEMINI_SKILLS_PATH="$GEMINI_SKILLS_PATH:/path/to/logical-fallacy-detector-agent-skill"
```

**3. That's it.** The skill ships with a pre-bundled `Logical_Fallacies_Vault/` directory. Once activated, your agent automatically indexes these Markdown files as its primary fallacy knowledge base — no further setup required.

> 💡 **Tip:** You can extend or customize the vault by adding your own `.md` fallacy definitions to `Logical_Fallacies_Vault/`.

---

## 📖 How to Call the Skill

Once activated in your agent, interact naturally:

**Analyze a quick snippet:**
> *"Analyze this: [Insert Argument]"*

**Run a full report:**
> *"--format markdown Review this essay for logical fallacies and produce a full report."*

**Batch process debate transcripts:**
> *"Analyze the following debate transcript for fallacies by speaker: [Transcript]"*

### Example Output (JSON)

```json
{
  "fallacy_detected": true,
  "type": "False Dilemma",
  "confidence": 0.91,
  "excerpt": "Either the government passes the law, or the country falls into chaos.",
  "explanation": "Presents only two options while ignoring viable alternatives.",
  "steelman": "The argument may be expressing urgency, but overstates the binary nature of the choice.",
  "repair": "Passing this law is one of several approaches that could help address rising crime rates."
}
```

---

## 🧠 How It Works

The skill follows a **three-phase pipeline** for every analysis:

1. **Steelman** — First attempts the most charitable interpretation of the argument. Only proceeds if a fallacy remains after this step.
2. **Classify** — Matches the reasoning error against definitions in the `Logical_Fallacies_Vault/`, returning a fallacy type and confidence score.
3. **Repair** — Generates a logically sound reconstruction of the original argument.

This design minimizes false positives and ensures the tool supports critical thinking rather than weaponizing it.

---

## 🗂️ Repository Structure

```
logical-fallacy-detector-agent-skill/
├── Logical_Fallacies_Vault/ # Curated Markdown definitions of fallacies
├── skill.md # Agent skill instruction file
└── README.md
```
---

## 🛠️ Built for augmented precision

- **Confidence Thresholds:** Adjustable precision levels (default 0.5).
- **Steelman Test:** Mandatory "Is there a non-fallacious version of this?" check.
- **Neutrality:** Politically agnostic, clinical analysis style.

---

## 🤝 Contributing

Contributions are welcome! To add new fallacy definitions, simply add a `.md` file to `Logical_Fallacies_Vault/` following the existing format. For feature additions, open an issue or submit a pull request.

---

## ⚖️ Licensing

**License:** Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0).

---

*“Logic is the beginning of wisdom, not the end.”*
