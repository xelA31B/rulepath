---
name: ai-act-check
description: >
  This skill should be used when the user asks "does the EU AI Act apply to us", "is our AI system
  high-risk", "classify our AI use under the AI Act", "what are our AI Act obligations", "AI Act deadlines
  for us", "are we a provider or deployer", or describes an AI system, product or internal AI use and wants
  to know which EU AI Act rules apply and by when. Also triggers on the same requests in Russian
  ("распространяется ли на нас AI Act", "к какому классу риска относится наша ИИ-система") or Hungarian.
metadata:
  version: "0.1.0"
---

# AI Act Check

Classify an AI system or AI use under the EU AI Act, identify the organisation's role, list the obligations that apply and the dates they apply from — with official sources.

## Rules

- Language of the user's request. Concise, professional, no filler.
- **Not legal advice.** State this once at the top of the report in one line and recommend legal review for high-risk or borderline cases.
- **Verify the law at every run.** Application dates and some obligations were amended (Regulation (EU) 2026/1744, the "Digital Omnibus on AI") and guidance keeps being published. Before reporting, use web search to confirm the current dates and any new Commission guidelines, preferring official sources (EUR-Lex, the AI Act Service Desk at ai-act-service-desk.ec.europa.eu, the European Commission's digital strategy site). Cite the article and source for every obligation. If official confirmation is unavailable, say so and mark the item **to verify**.
- Every conclusion follows **article → facts from the user → reasoning**. When facts are missing, ask; do not assume a lower risk class.
- Do not invent article numbers or dates. If unsure, mark **to verify** and point to the official AI Act Explorer.

## Step 1 — Facts

Ask in one short message only for what is missing (see `references/classification-guide.md` for the full list):

- What the system does, its intended purpose, who uses it and who is affected
- Whether the organisation develops it, puts it on the market under its own name, or only uses it (role)
- Where it is placed on the market or used (EU / outside the EU with output used in the EU)
- Sector and use case (employment, education, credit, biometrics, critical infrastructure, health, public services, law enforcement, etc.)
- Whether it is a general-purpose AI model, interacts with people, or generates or manipulates content
- Whether it is a safety component of a product covered by EU product legislation

## Step 2 — Classify

Follow `references/classification-guide.md` in order:

1. In scope? (AI system definition, territorial scope, exclusions)
2. Role(s): provider, deployer, importer, distributor, authorised representative, product manufacturer
3. Prohibited practice?
4. High-risk: Annex I (product safety) or Annex III (use cases), including the Article 6(3) derogation and its documentation duty
5. Transparency obligations (Article 50)
6. General-purpose AI model obligations (and systemic risk)
7. Horizontal duties that apply to everyone (e.g. AI literacy — check its current wording after the amendments)

## Step 3 — Report

Deliver the branded report (`references/report-template.md`) when HTML output is available; otherwise:

```
# AI Act Check — [system] · [date]
_Not legal advice. Dates verified against [source] on [date]._

**Classification:** Prohibited / High-risk (Annex I|III) / Transparency / Minimal · **Role:** …
One-line reason.

## Obligations that apply
| # | Obligation | Article | Applies from | Who | Status (to do / in place / to verify) |

## Key dates for you
| Date | What applies |

## Missing facts / borderline points
- …

## Sources
- official links used
```

Close with one line offering: generate the governance documents (`ai-policy-pack`) or review existing documents against these obligations (`ai-gap-review`).

## Recurring run

At the end of the report, offer a recurring run. Recommended cadence: quarterly, plus whenever the system's purpose, users or market change, and before each AI Act application date.

Let the user choose their own schedule. Ask in one short message, with the recommendation pre-filled:

- **Frequency:** daily · weekly · every 2 weeks · monthly · quarterly · custom
- **Day:** e.g. Monday, Friday, 1st of the month
- **Time and time zone:** e.g. 09:00 Europe/Budapest (use the user's time zone if known)
- **Delivery:** in this chat, a new chat, or a document

If the environment offers scheduled tasks (a scheduling tool is available), create the task only after the user confirms these choices. Write the scheduled prompt so it is self-contained: what to check, which skill to run, the report language, and where to deliver the result. Confirm what was scheduled in one line. The user can change or cancel the schedule at any time; when asked, update or remove it.

If no scheduling tool is available, state the chosen or recommended cadence and suggest a calendar reminder.
