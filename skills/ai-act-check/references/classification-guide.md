# EU AI Act classification guide

Regulation (EU) 2024/1689, as amended by Regulation (EU) 2026/1744. **Always verify articles, annex items and dates against the official text (EUR-Lex) and the AI Act Service Desk before reporting.** This guide gives the order of reasoning, not the final law.

## Official sources

| Source | Use |
|---|---|
| EUR-Lex — Regulation (EU) 2024/1689 and amending Regulation (EU) 2026/1744 | Binding text |
| AI Act Service Desk (ai-act-service-desk.ec.europa.eu) | Official Compliance Checker, AI Act Explorer, FAQs, guidance, timeline, question form |
| European Commission guidelines (AI system definition, prohibited practices, high-risk classification, GPAI) | Interpretation |
| National market surveillance / competent authorities | Local enforcement and contacts |

## Facts to collect

1. Intended purpose and actual use; users; affected persons
2. Technique (does it infer outputs such as predictions, content, recommendations or decisions with some autonomy?)
3. Role of the organisation for this system
4. Market: placed on the EU market, put into service in the EU, or output used in the EU
5. Sector and use case
6. Product link: safety component of, or itself, a product under Annex I legislation (e.g. machinery, toys, medical devices, radio equipment, vehicles)
7. Interaction with natural persons; emotion recognition or biometric categorisation; generated or manipulated content (text, image, audio, video)
8. General-purpose AI model: trained on broad data, generally capable; compute and systemic-risk indicators
9. Exclusions: military/defence/national security only, scientific research only, personal non-professional use, certain open-source releases

## Order of reasoning

1. **Scope** — AI system definition (Art. 3), territorial scope (Art. 2), exclusions.
2. **Roles** — provider, deployer, importer, distributor, authorised representative; when a deployer becomes a provider (substantial modification, own name, changed purpose).
3. **Prohibited practices** (Art. 5) — check each listed practice, including the practices added by the 2026 amendment. If any applies: stop, classify as prohibited.
4. **High-risk**
   - Annex I route: safety component of / product under listed Union harmonisation legislation requiring third-party conformity assessment.
   - Annex III route: listed use cases (biometrics; critical infrastructure; education and vocational training; employment and workers management; access to essential private and public services incl. credit and insurance; law enforcement; migration, asylum and border control; administration of justice and democratic processes).
   - Article 6(3) derogation: an Annex III system may be not high-risk if it does not pose a significant risk (narrow procedural task, improves a completed human activity, detects patterns without replacing human assessment, preparatory task) — never when it profiles natural persons. Document the assessment; check current registration duties.
5. **Transparency** (Art. 50) — interaction with AI, synthetic content marking, deepfakes, emotion recognition/biometric categorisation notices.
6. **GPAI models** (Chapter V) — documentation, copyright policy, training-content summary; additional duties for systemic-risk models; codes of practice.
7. **Everyone** — AI literacy (check current wording after amendment), voluntary codes of conduct for minimal-risk systems.

## Main obligations to map (verify each)

**Provider of high-risk system:** risk management system; data and data governance; technical documentation; record-keeping/logging; transparency and instructions for use; human oversight; accuracy, robustness, cybersecurity; quality management system; conformity assessment; EU declaration of conformity and CE marking; registration in the EU database; post-market monitoring; serious-incident reporting; corrective actions.

**Deployer of high-risk system:** use per instructions; competent human oversight; input data relevance; monitoring and logs retention; informing workers and affected persons; fundamental-rights impact assessment where required (public bodies, certain private services such as credit and insurance); cooperation with authorities.

## Dates (verify at every run)

As amended by Regulation (EU) 2026/1744 (in force 27 July 2026):

| Date | What applies |
|---|---|
| 2 Feb 2025 | Prohibitions; AI literacy |
| 2 Aug 2025 | GPAI model obligations; governance; penalties framework |
| 2 Aug 2026 | General application, including Article 50 transparency (with exceptions below) |
| 2 Dec 2026 | Newly added prohibitions; marking of AI-generated content (legacy systems) |
| 2 Dec 2027 | High-risk obligations for Annex III systems |
| 2 Aug 2028 | High-risk obligations for Annex I (product-embedded) systems |

Further transitional dates exist for systems already on the market and for public-sector legacy systems; check the consolidated text.

## Penalties (orientation)

Fines are tiered by infringement type (prohibited practices highest, then other obligations, then incorrect information), with adjusted treatment for SMEs. Quote the exact amounts only from the official text.
