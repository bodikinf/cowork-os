> **EN —** Your drop zone. Dump anything unsorted here — notes, docs, PDFs, exports, screenshots — then tell Claude **"process the inbox"**. Claude reads it all, files the facts into the right modules, and reports what it learned and what's still missing. Nothing is deleted without asking.
> **IT —** La tua zona di scarico. Butta qui qualsiasi cosa non ordinata — note, documenti, PDF, export, screenshot — poi di' a Claude **"processa l'inbox"**. Claude legge tutto, archivia i fatti nei moduli giusti e ti dice cosa ha capito e cosa manca. Niente viene cancellato senza chiedere.

---

## The "dump, don't fill forms" setup path · Configurare scaricando, non compilando

Don't have time to fill in `context/` by hand? This is the second way to set up: **drop everything here and let Claude organize it.**

1. Put files in this folder (or paste links/notes in chat).
2. Say: **"processa l'inbox"** / "process the inbox".
3. Claude reads everything → extracts the facts → writes them into the right files → leaves a short report → asks before moving or deleting anything.

## Instructions to Claude (when asked to process this folder)

- Treat every file/link here as **raw, unorganized input**. Don't assume structure.
- **Route the facts** to the most specific file:
  - company facts, market, status → `context/overview.md`
  - value proposition, messages, differentiation → `context/positioning.md`
  - offers, services, pricing, use cases → `context/services.md`
  - voice, words to use/avoid → `context/tone_of_voice.md`
  - campaigns, analytics, ad data → `marketing/`
  - site structure, copy, SEO, UX notes → `website/`
  - decisions and assumptions → `decisions/`
  - anything about an owned product → `products/`
- **Separate facts / assumptions / open questions.** Never invent; if a fact is missing, add it to `decisions/open_questions.md`.
- **Report back** a small table — `source → filed in → confidence` — plus the top open questions and what you still need from the user.
- **Be non-destructive:** keep the originals, keep an index of what you processed, and **ask before moving or deleting** anything.

> Keep this folder out of your public repo if you dump private material here (it's already covered by `.gitignore` patterns you can enable).
