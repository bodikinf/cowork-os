---
description: Run the Memory Update protocol. Checks whether decisions, questions, assumptions, risks, tasks, or opportunities emerged in the current task and writes them to the right files, then prints the required end-of-task summary.
---

# /cowork-os:memory-update

Run the **Memory Update** protocol that keeps this workspace a living knowledge base instead of a disposable chat.

Before considering the current task done, check whether any of these emerged: decisions, open questions, assumptions, risks, tasks, commercial opportunities, roadmap updates, stale information, source conflicts. If something relevant emerged, update the right file.

## Where to write what
- confirmed decisions: `decisions/decisions_log.md`
- open questions: `decisions/open_questions.md`
- unvalidated assumptions: `context/assumptions.md` if present, else `decisions/open_questions.md`
- positioning insight: `context/positioning.md`
- tone-of-voice notes: `context/tone_of_voice.md`
- general marketing insight: `marketing/strategy.md`
- campaign insight: `marketing/campaigns.md`
- content ideas: `marketing/content.md`
- data, analytics, reports: `analytics/` or `reviews/`
- website tasks: `website/backlog.md`
- website, SEO, UX, conversion notes: `website/website_notes.md`
- risks: `strategy/risks.md` if present, else `decisions/open_questions.md`
- opportunities: `business-development/` if present, else `marketing/strategy.md`
- partnerships: `business-development/partnerships.md` if present, else `decisions/open_questions.md`
- operational reviews: `reviews/weekly_review.md` or `reviews/maintenance_review.md`

If you cannot edit files directly, do not skip the Memory Update: return a section with the recommended changes (file to update, content to add, content to change, content to verify, reason). If nothing changed, state it explicitly: "Memory Update: nothing to update."

## Required end-of-task format
```
Memory Update
- Files updated:
- Decisions added:
- Open questions added:
- Assumptions added:
- Tasks added:
- Risks added:
- Opportunities added:
- Next actions:
```
