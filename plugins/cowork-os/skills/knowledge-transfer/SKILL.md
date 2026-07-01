---
name: knowledge-transfer
description: Interview a person and turn their operating know-how (tacit knowledge) into the company brain: processes, rules with source, a glossary, decisions and open questions, written into the workspace. Use whenever someone needs to capture how a process actually gets done, before a key person leaves or retires, to onboard a new hire faster, to standardize a workflow, or to rescue knowledge that lives in one head ("only Marco knows how to do it"). Triggers: onboarding, a key person leaving or retiring, bus factor, tribal knowledge, "document how we do X", "capture what the expert knows", map a workflow, standardize a process, write SOPs by talking to the person who does the job.
---

# Knowledge Transfer, the interview that builds the company brain

You interview one person and turn their tacit know-how into the workspace, so the team and other agents can read, apply and correct it.

**The hard truth this skill exists for:** people cannot narrate a process they have automated. The better someone is at a job, the less they can explain it, because they run it on autopilot. Ask "how do you do X" and you get the **official, abstract** version (the manual), not the **real** one (the one full of "well, it depends"). Your job is not to collect answers. It is to make the tacit **observable**. Interview in the user's language.

## Non-negotiables
- **One question at a time.** Never a volley. Short questions.
- **Never invent.** Every rule carries a source (interview, date, who) and a confidence. If something is unknown, say so and park it in `decisions/open_questions.md`.
- **After the first 3-4 framing questions, stop using a list.** Generate every next question **from the person's last answer**, aimed at its vaguest or most loaded part. A generic follow-up you could have asked anyone is a failure.
- **Budget: about 15 minutes, 1 or 2 processes per session.** Depth over coverage. The brain grows over more sessions, do not try to capture everything at once.

## Step 1, frame (standard, 3-4 questions only)
- Who you are and your role, which single process we capture today.
- **Objective:** what must a new hire be able to **do** on their own within 2 weeks? (this fixes the scope)
- Which case is most frequent, and which one hurts most if done badly? (pick ONE to start)
- **Start from a real episode:** "Think of the LAST time you did this. Walk me through that specific time, step by step." Never start from the abstract "how do you usually do it".

## Step 2, the probing loop (this is the actual skill)
For the chosen process, run this loop until you have concrete rules, then move to the next step or process. Each turn: read the last answer, pick the probe that attacks what is missing, ask ONE short question.

Probe library (choose by what the last answer lacked):
- **Real case, not abstract.** Keep anchoring to a specific instance: "the last time...", "an example from this week".
- **Pounce on hedge words.** When they say *usually, normally, it depends, obviously, just, more or less, you get a feel for it, then you see* — that is compiled tacit knowledge surfacing. Dig immediately. Example: they say "usually I approve the return if it's within terms" -> "You said 'usually'. When do you NOT approve it even within terms? And when do you approve it even out of terms?"
- **Contrast with a novice.** "What would a new hire do here that looks right but is wrong? Why don't you do that?" Surfaces the unwritten rule by contrast.
- **Chase the decision points.** At each step: "what could go differently here? how do you decide between A and B, exactly?" The branches are where the expertise lives.
- **Official vs real.** "That is the procedure on paper. What actually happens when you're slammed, or the case is weird?" The gap between the two is pure tacit knowledge.
- **Ask for the artifact.** "Show me the actual email / ticket / file from that time" instead of a description. The real object jogs the steps the story drops.

**Target per branch:** a rule = `trigger` + `action` + at least one `exception` + the `decision criterion` + `source`.
**Stop condition per branch:** once you have that, move on. Do not over-mine one point, and do not leave it vague either.

## Step 3, reconstruct and correct (every 3-4 exchanges)
People are bad at generating their own process and great at correcting a proposed one. So do not only ask, **hypothesize and reflect back**: "So the flow is A, then B, then C, and the tricky part is B when X happens. Right?" Let them fix it. This is how you show a person a workflow they did not know they were following.

## Step 4, verify and close
Mirror back 5-8 key rules as trigger / action / exception and let the person correct until confirmed. Then write.

## If the know-how belongs to someone else
The person who installed cowork-os is often not the expert. If the process lives in someone else's head, do not fake it. Produce a ready-to-use **interview plan** for the real expert: the objective, the one process, and 8-12 tailored opening probes that follow the loop above. Offer to run the interview live with them, or to capture their answers when available. Write the plan to `context/processes/<process>_interview-plan.md`.

## Output: write it into the workspace (the company brain)
Write the extracted knowledge into the cowork-os folders (create files if missing):
- `context/processes/<process>.md` — the readable source of truth: objective, when it applies, the real step-by-step, the decision points, the exceptions and edge cases, the unwritten rules, links to the rules in the log, source (who and when), open questions, last updated.
- `context/glossary.md` — internal terms, system names, acronyms that came up.
- `decisions/decisions_log.md` — each rule as a decision with a status, phrased as `trigger -> action`, with `exceptions`, and `source: interview with <role>, <date>, "<quote>"`, and a confidence (`high` = said explicitly, `medium` = synthesis, `needs_review` = inferred; only high and medium are used in production).
- `decisions/open_questions.md` — gaps that emerged, to clarify with other people.

Optional, for agent consumption: `context/knowledge/rules.jsonl`, one rule per line (id, type, domain, trigger, action, exceptions, anti_patterns, source, confidence). Keep the human `context/processes/*.md` as the readable source of truth.

## Validate (optional but recommended)
After the interview, generate 5-10 test cases from the extracted know-how ("given this scenario, what does the rule do?") and check that an agent applies the right rule and respects the exceptions. It is the only way to know the company brain actually learned instead of improvising.

## Example probes, domain: customer care / support
- **Frame:** what must a new support agent handle alone in 2 weeks? Which 3 request types are 80% of volume? Which one loses the customer if mishandled? Walk me through the last hard one.
- **Loop:** when do you NOT follow the standard script? How do you tell a customer must be calmed before being solved? What is the exact threshold to escalate to a senior or a human? What is the difference between a correct answer and one the customer actually accepts? What do you do when you do not know, and what must you never promise? What does a new hire get wrong that looks fine? Unwritten tone rules, what to never say? Edge cases: out-of-policy return, rightly angry customer, ambiguous request, double order.
- **Reconstruct:** "So: request arrives, you check A, then B, and you escalate when X unless Y. Right?"

> To add a domain (sales, admin, operations, production): keep the same loop and swap only the domain-specific probes. The engine does not change.

## Close with a Memory Update
End with the cowork-os Memory Update: list what you wrote (processes, decisions and rules, glossary terms, open questions) and where. Run `/cowork-os:memory-update` for the full protocol, or do it inline.
