---
name: ai-policy-pack
description: >
  This skill should be used when the user asks to "write an AI policy for our company", "create an AI
  governance framework", "AI acceptable use policy", "AI system register / inventory", "AI risk assessment
  template", "AI literacy training plan", "prepare for ISO 42001", "NIST AI RMF implementation", or wants
  governance documents for responsible and compliant use of AI. Also triggers on the same requests in
  Russian ("политика использования ИИ в компании", "регламенты для ИИ", "реестр ИИ-систем") or Hungarian.
metadata:
  version: "0.1.0"
---

# AI Policy Pack

Produce a practical set of AI governance documents tailored to the organisation, aligned with the EU AI Act, the NIST AI Risk Management Framework and the structure of ISO/IEC 42001.

## Rules

- Language of the user's request (or the language the documents must be in, if different).
- Concise, professional, usable. No boilerplate the organisation will not apply. Each requirement in a document traces to a source: **AI Act article**, **NIST AI RMF function/category** or **ISO/IEC 42001 clause/control area**.
- **Not legal advice**; note once that documents should be reviewed by the organisation's legal or compliance function.
- Verify current AI Act obligations and dates by web search against official sources before drafting (same rule as `ai-act-check`).
- ISO/IEC 42001 is a paid standard: reference its public structure (clauses 4–10, Annex A control areas) and do not reproduce its text.
- Use only facts the user gives; mark assumptions **to confirm**.

## Step 1 — Profile

Ask in one short message only for what is missing:

- Organisation size, sector, countries
- How AI is used: internal tools (e.g. chat assistants, coding), AI in products, AI for decisions about people
- Roles under the AI Act (from `ai-act-check` if run)
- Target: internal governance only, AI Act readiness, NIST alignment, or ISO/IEC 42001 certification path
- Existing policies to align with (information security, data protection/GDPR, procurement)

## Step 2 — Select documents

Default set (adapt to the profile; see `references/document-set.md`):

1. **AI Policy** — principles, scope, roles and responsibilities, approval and escalation
2. **AI Acceptable Use Rules** — for employees using AI tools: allowed, restricted, prohibited uses; data handling
3. **AI System Register** — fields for an inventory of AI systems and uses (as a table)
4. **AI Risk & Impact Assessment template** — per system; aligned with NIST Map/Measure and AI Act requirements
5. **AI Literacy Plan** — audiences, topics, frequency, evidence
6. **AI Incident Procedure** — detection, triage, serious-incident reporting where required, lessons learned
7. **Transparency notices** — wording for AI interaction and AI-generated content where Article 50 applies
8. **Supplier / procurement checklist** — questions for AI vendors
9. **Crosswalk** — table mapping each document section to AI Act articles, NIST functions and ISO 42001 clauses

## Step 3 — Deliver

Create the documents as one document artifact (or separate files) when available, otherwise in chat. Start with a one-page index: document, purpose, owner, review cycle. Keep each document short and actionable.

Close with one line offering a gap review of the organisation's current state against these documents (`ai-gap-review`).

## Recurring run

Recommended cadence: review the pack every 6 months, and after any AI Act guidance or date change or a new AI system. Offer the same scheduling options as `ai-act-check` (frequency, day, time and time zone, delivery), create a scheduled task only after the user confirms, and let them change or cancel it at any time. If no scheduling tool is available, state the cadence and suggest a calendar reminder.
