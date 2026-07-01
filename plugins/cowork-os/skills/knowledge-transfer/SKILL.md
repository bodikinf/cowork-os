---
name: knowledge-transfer
description: Interview a person and turn their operating know-how (tacit knowledge) into the company brain: processes, rules with source, a glossary, decisions and open questions, written into the workspace files. Use whenever someone needs to capture what a person knows before they leave or retire, onboard a new hire faster, standardize how a task is done, or rescue knowledge that lives in one head ("only Marco knows how to do it"). Triggers: onboarding, a key person leaving or retiring, tribal knowledge, "document how we do X", "capture what the expert knows", knowledge transfer, standardize a process, write SOPs by talking to the person who does the job.
---

# Knowledge Transfer, the interview that builds the company brain

You conduct a structured interview with one person, extract their tacit know-how (the exceptions, the decision criteria, the unwritten rules), and write it into the cowork-os workspace so the team and other agents can read, apply and correct it. Interview in the user's language.

## What this is (and is not)
- **Is:** one question at a time, dig into what is not written down, then write it into the workspace as processes, rules with a source, a glossary and open questions.
- **Is not:** a transcribed chat, a fixed questionnaire, or invented content. Every rule carries a source (interview, date, who said it) and a confidence level. If you do not know, say so.

## Principle: objective-first, one question at a time
Do not start from tasks. Start from the goal: what must a new hire (or an agent) be able to **do** on their own at the end? That fixes the scope. Then guide the person through their real processes, generating follow-ups from their answers, not from a fixed list. Close every block by mirroring back and letting them correct.

## The conductor: 4 phases
**Phase 0, setup (30s).** Who are you, what role, which process/area today, how long we have.

**Phase 1, objective.** One question at a time: what result must this knowledge produce? What must a new hire do alone within 2 weeks? Which 3 cases are most frequent, and which 3 do most damage if handled badly? This is the distillation scope.

**Phase 2, process map.** Take the most frequent case: how does the request arrive (channel)? What do you do first? Step by step to closing. Which systems do you open, in what order? Where do you wait on someone else? Repeat for the 2-3 key processes.

**Phase 3, laddering (this is where the value is).** On each process, dig: when do you NOT do it this way (the exceptions are the tacit knowledge)? How do you choose between A and B, the exact criterion? What mistake do new people make that looks small but costs a lot? What is an unwritten rule no manual states? What do you do when you do not know the answer, and what must you never promise?

**Phase 4, verify.** Mirror back 5-8 key rules and let the person correct: "so the rule is: do X, except when Y, right?" Repeat until confirmed.

## How to interview well
- One question at a time. No volleys.
- Follow-ups from the answer, not from a script.
- Speak the person's language, no jargon.
- Push on exceptions and decision criteria, that is the know-how nobody wrote down.
- Do not fill silences with your own interpretation, ask.
- Close each block by mirroring and letting them correct.

## Output: write it into the workspace (the company brain)
Write the extracted knowledge into the existing cowork-os folders (create files if missing):
- `context/processes/<process>.md` — the step-by-step for each process, in plain language.
- `context/glossary.md` — internal terms, system names, acronyms.
- `decisions/decisions_log.md` — each rule as a decision with a status, phrased as `trigger -> action`, with `exceptions`, and `source: interview with <role>, <date>, "<quote>"` and a confidence (`high` = said explicitly, `medium` = synthesis, `needs_review` = inferred; only high/medium are used in production).
- `decisions/open_questions.md` — gaps that emerged, to clarify with other people.

Optional, for agent consumption: `context/knowledge/rules.jsonl`, one rule per line (id, type, domain, trigger, action, exceptions, anti_patterns, source, confidence). Keep the human `context/processes/*.md` as the readable source of truth.

## Validate (optional but recommended)
After the interview, generate 5-10 test cases from the extracted know-how ("given this scenario, what does the rule do?") and check that an agent applies the right rule and respects the exceptions. It is the only way to know the company brain has actually learned instead of improvising.

## Example question bank, domain: customer care / support
**Objective:** what must a new support agent handle alone within 2 weeks? Which 3 request types are 80% of volume? Which 3 situations lose the customer if mishandled?
**Process map:** most common request, which channel, what do you check first, then, until you consider it closed? Which systems, in what order, where do you have to ask someone else?
**Laddering:** when do you NOT follow the standard script? How do you tell if a customer must be calmed before being solved? What is the exact threshold to escalate to a senior/human? What is the difference between a correct answer and one the customer actually accepts? What do you do when you do not know, and what must you never promise? A new-hire mistake that looks small but costs a lot? Unwritten tone rules, what to never say to a customer? Edge cases: out-of-policy return, rightly angry customer, ambiguous request, double order.
**Verify:** mirror 5-8 rules ("escalate when X, unless Y, right?") and let them correct.

> To add a domain (sales, admin, operations): duplicate this block and rewrite only the laddering questions. The phased skeleton stays identical.

## Close with a Memory Update
End with the cowork-os Memory Update: list what you wrote (processes, decisions/rules, glossary terms, open questions) and where. Run `/cowork-os:memory-update` for the full protocol, or do it inline.
