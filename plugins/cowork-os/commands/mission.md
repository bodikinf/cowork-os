---
description: Start or advance a mission, an ambitious outcome (a dream client, a partnership, breaking into named accounts) that Claude pursues as an outcome, not a task, with route maps, an evidence log, and stop conditions.
argument-hint: "[mission name or goal]"
---

# /cowork-os:mission

Run "mission mode": for an ambitious goal, pursue the OUTCOME, not a single task. Refuse to stop at "I sent the email."

If a mission name or goal is given ($ARGUMENTS), start or advance it. Otherwise ask for the goal.

1. Define the outcome in one measurable sentence (what counts as done).
2. Map 2-4 routes to the outcome (parallel paths, not a single plan).
3. For each route, list the next concrete action and what evidence would prove progress.
4. Keep an evidence log: what was tried, what happened, what it means.
5. Set stop conditions: what tells you to drop a route or escalate.
6. Create or update the mission file under `missions/<slug>/` from the template if the folder exists; otherwise propose creating `missions/`.
7. Recommend the mission-weekly-review routine to keep it moving.

End with a Memory Update (decisions to `decisions/decisions_log.md`, risks and questions to `decisions/open_questions.md`).
