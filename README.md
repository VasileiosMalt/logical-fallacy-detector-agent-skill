# Fallacy Detector Agent

A specialized agent for identifying, analyzing, and explaining logical fallacies in any text, powered by a structured knowledge base of fallacies.

## Features

- **Automated Fallacy Detection:** Scans text to identify structural and reasoning errors.
- **Obsidian Vault Integration:** Dynamically loads logical fallacy definitions from local Markdown files.
- **Evidence-Based Analysis:** Uses a confidence-scoring system to minimize false positives.
- **Charitable Repair:** Provides "steelman" versions of arguments and repair suggestions.
- **Structured Output:** Generates machine-readable JSON or human-readable Markdown reports.
- **Neutrality & Rigor:** Strictly differentiates between rhetoric and genuine fallacies.

## Quick Start

### Prerequisites
- This agent expects a directory containing logical fallacy definitions in Markdown format (e.g., `Logical_Fallacies_Vault/`).

### Configuration
The agent automatically scans for a `Logical_Fallacies_Vault` directory in the current working directory. You can override the path if necessary.

### Usage
Analyze an argument:
```
Analyze this for logical fallacies: "You can't trust climate scientists because they get government funding."
```

Analyze with a report format:
```
--format markdown
Review this essay for logical fallacies and produce a full report.
```

## How It Works

1. **Vault Scan:** Locates and loads fallacy definitions from your Obsidian vault or the built-in catalog.
2. **Argument Reconstruction:** Identifies premises, implicit assumptions, and intended conclusions.
3. **Analysis:** Compares the reconstructed argument against the loaded fallacy base.
4. **Charitable Interpretation:** Attempts to "steelman" the argument before flagging it.
5. **Reporting:** Outputs findings with confidence scores, verbatim passages, and repair suggestions.

## Contributing

This agent is designed to be easily extensible. To add new fallacy definitions, simply create a new Markdown file in the `Logical_Fallacies_Vault/` directory.

## License

MIT
