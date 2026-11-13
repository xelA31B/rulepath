# Rulepath — Claude plugin

EU AI Act and AI governance without guesswork. Rulepath classifies your AI systems, tells you which obligations apply and from when — verified against official sources at every run — and produces the governance documents and gap reviews to get there.

_Rulepath supports compliance work; it is not legal advice._

## Install

**Claude app (web, desktop):** Plugins → add a marketplace from a GitHub repository → `xelA31B/rulepath` → install **Rulepath**. Once approved in the Claude directory, search for **Rulepath** in Plugins.

**Claude Code (VS Code or terminal):**

```
/plugin marketplace add xelA31B/rulepath
/plugin install rulepath@rulepath
```

## Commands

Type `/` in Claude and pick a command:

| Command | What it does |
|---|---|
| `/ai-act-check [AI system or use case]` | Classification (prohibited / high-risk / transparency / minimal), your role, obligations with articles and current dates |
| `/ai-policy-pack [organisation and AI use]` | AI policy, acceptable-use rules, AI system register, risk and impact assessment, literacy plan, incident procedure, transparency notices, supplier checklist, crosswalk |
| `/ai-gap-review [documents or scope]` | Evidence-based gap review with a dated action plan |

## Sources

| Source | Use |
|---|---|
| EUR-Lex — Regulation (EU) 2024/1689 as amended by Regulation (EU) 2026/1744 | Binding text |
| EU AI Act Service Desk — Compliance Checker, AI Act Explorer, FAQs, guidance | Official interpretation and timeline |
| NIST AI Risk Management Framework, Playbook, Generative AI Profile | Risk management functions and actions |
| ISO/IEC 42001 (public structure) | Management system clauses and control areas |

Application dates and guidance change. Rulepath checks them with web search against official sources before every report and marks anything it cannot confirm as "to verify".

## Reports

Concise, evidence-based reports in the language of your request, delivered as a branded report where supported. Schedule regular re-checks on your own frequency, day and time.

## License

MIT
