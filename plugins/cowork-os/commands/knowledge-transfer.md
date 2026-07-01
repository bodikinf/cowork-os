---
description: Interview a person to capture their operating know-how (tacit knowledge) and write it into the workspace as the company brain: processes, rules with source, glossary, decisions and open questions. For onboarding, a key person leaving, or standardizing a process.
argument-hint: "[who / which process, e.g. 'our warehouse lead, the returns process']"
---

# /cowork-os:knowledge-transfer

Run a structured, objective-first interview and build the company brain from one person's knowledge. Interview in the user's language. Use `context/tone_of_voice.md` if present.

Who / what to capture: $ARGUMENTS. If empty, ask who you are interviewing and which process or area before starting.

Run these phases (one question at a time, never a volley):
1. **Setup:** role, process/area, time available.
2. **Objective:** what must a new hire do alone in 2 weeks? Which 3 cases are most frequent, which 3 most costly if mishandled?
3. **Process map:** for each key process, step by step from request to closing; systems used and in what order; where they wait on someone.
4. **Laddering (the value):** exceptions ("when do you NOT do it this way?"), decision criteria, typical new-hire mistakes, unwritten rules, what to never promise.
5. **Verify:** mirror back 5-8 rules ("do X, except when Y, right?") and let them correct.

Then write into the workspace:
- `context/processes/<process>.md` (readable step-by-step)
- `context/glossary.md` (internal terms)
- `decisions/decisions_log.md` (rules as `trigger -> action` + `exceptions` + `source: interview, <date>` + confidence)
- `decisions/open_questions.md` (gaps to clarify)

Never invent. Every rule carries a source and a confidence; if unknown, say so. Optionally generate 5-10 test cases to check an agent applies the rules correctly.

End with a Memory Update listing what you wrote and where.
