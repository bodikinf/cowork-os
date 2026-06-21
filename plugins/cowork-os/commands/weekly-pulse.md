---
description: Produce the weekly marketing pulse, a short Monday brief on what marketing did last week and the priorities for this week, grounded in the workspace memory and any connected analytics.
---

# /cowork-os:weekly-pulse

Produce a short **weekly marketing pulse**: a Monday brief on what marketing did and the week's priorities.

1. Read `marketing/strategy.md`, `marketing/campaigns.md`, `marketing/content.md`, and the latest file in `reviews/` if present.
2. If analytics or ads connectors are connected, pull the key numbers for the last 7 days. If not, say so and work from the workspace memory. Never invent numbers.
3. Output three blocks: (a) what happened last week, facts only; (b) what it means, 2-3 reads; (c) the 3 highest-impact priorities for this week, each with a concrete next action and an owner.
4. Keep it short and scannable. Separate facts, assumptions, and recommendations.

End with a Memory Update (file the brief in `reviews/`, route new insight to `marketing/strategy.md`).

This is meant to run on a schedule (suggested cadence: Monday 08:00). Offer to set it up as a scheduled task.
