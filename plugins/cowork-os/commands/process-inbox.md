---
description: Process the _inbox. Read everything the user dropped in (notes, links, a deck, a messy folder) and route each fact to the most specific workspace file, separating facts from assumptions and open questions, without inventing anything.
---

# /cowork-os:process-inbox

The user has unsorted material. Organize it into the workspace.

1. Read everything in `_inbox/` (and any links or notes the user pasted). If `_inbox/` does not exist, ask them to drop material there or paste it.
2. Extract the facts. Route each to the most specific file:
   - company, market, status: `context/overview.md`
   - value proposition, messages, differentiation: `context/positioning.md`
   - offers, pricing, use cases: `context/services.md`
   - voice: `context/tone_of_voice.md`
   - campaigns, analytics: `marketing/`
   - site, copy, SEO: `website/`
   - decisions and assumptions: `decisions/`
   - owned products: `products/`
3. Separate facts, assumptions, and open questions. Never invent. Missing facts go to `decisions/open_questions.md`.
4. Be non-destructive: keep originals, ask before moving or deleting.
5. Report a short table: source, filed-in, confidence.

End with a Memory Update.
