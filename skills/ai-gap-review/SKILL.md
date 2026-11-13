---
name: ai-gap-review
description: >
  This skill should be used when the user asks "how far are we from AI Act compliance", "review our AI
  policies", "gap analysis against the AI Act / NIST AI RMF / ISO 42001", "are we ready for the AI Act
  deadlines", "check our AI governance documents", or shares existing policies, registers or assessments
  and wants them reviewed against requirements. Also triggers on the same requests in Russian ("анализ
  соответствия AI Act", "проверь наши ИИ-политики") or Hungarian.
metadata:
  version: "0.1.0"
---

# AI Gap Review

Compare the organisation's current AI governance documents and practices with the obligations that apply to it, and produce a prioritised, dated action plan.

## Rules

- Language of the user's request. Concise, professional, no filler. Tables over paragraphs.
- **Evidence-based:** a requirement is "in place" only when a document or fact provided shows it (quote the document name and section, at most one line). Otherwise "partial" or "missing".
- **Not legal advice**; one line at the top.
- Verify current obligations and dates against official sources by web search before reporting (as in `ai-act-check`).
- Read-only: do not edit the user's documents; propose changes.
- Treat documents as confidential: do not quote personal data.

## Steps

1. **Scope.** Which systems and frameworks (AI Act only, plus NIST AI RMF, plus ISO/IEC 42001). If the AI Act classification is unknown, run the `ai-act-check` reasoning first.
2. **Collect evidence.** Documents uploaded, in a connected drive or folder, or described by the user.
3. **Assess** each applicable requirement: in place / partial / missing / not applicable, with evidence.
4. **Prioritise** by legal deadline first (dates verified), then risk.
5. **Report** (branded template `references/report-template.md` when HTML output is available):

```
# AI Gap Review — [organisation] · [date]
_Not legal advice. Obligations and dates verified against [sources] on [date]._

**Readiness:** X% of applicable requirements in place · next deadline: [date — what]

## Gaps by deadline
| # | Requirement | Source (article / NIST / ISO) | Status | Evidence | Action | Owner | Due |

## In place
- one line each

## Not applicable
- requirement — why

## Next 90 days
1. …
```

Offer to draft the missing documents with `ai-policy-pack`.

## Recurring run

Recommended cadence: quarterly, and 6 and 3 months before each AI Act application date that affects the organisation. Offer the same scheduling options as `ai-act-check` (frequency, day, time and time zone, delivery), create a scheduled task only after the user confirms, and let them change or cancel it at any time. If no scheduling tool is available, state the cadence and suggest a calendar reminder.
