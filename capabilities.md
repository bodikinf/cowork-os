# Capabilities catalog · Catalogo delle capacità

> **EN —** The "brain" the installer reasons over. For every module, automation and skill: what it is in plain language, **when to set it up** (triggers from the interview), and what it creates. Claude reads this to *proactively* propose the right setup — because the average user doesn't know these features exist.
> **IT —** Il "cervello" su cui ragiona l'installer. Per ogni modulo, automazione e skill: cos'è in parole semplici, **quando attivarlo** (trigger dall'intervista) e cosa crea. Claude legge questo per proporre *in modo proattivo* il setup giusto — perché l'utente medio non sa che queste funzioni esistono.

**How Claude should use this file:** during the interview, match the user's answers to the `Trigger` of each item below. Propose every match in plain language with a one-line *why it fits them*, grouped, and let them deselect. Default to "yes" for anything clearly relevant. Never wait for the user to ask for a capability they don't know exists.

**Two companions:** read **`examples/yempik/`** as the *quality bar* — a complete, real, sanitized workspace showing what "good" looks like. And remember the **`_inbox/`** drop-zone: if the user has unsorted material, have them dump it there and say *"process the inbox"* instead of answering everything by hand.

---

## 1. Core (always set up)

| Capability | What it is (plain language) | Creates |
|---|---|---|
| **Living memory** | The project keeps decisions, open questions and context in files you can read and correct, so the workspace compounds week over week instead of starting from zero. | `context/`, `decisions/`, the **Memory Update** habit in `PROJECT_INSTRUCTIONS.md` |
| **Project Instructions** | The system prompt that makes Claude check sources, separate facts from assumptions, and update memory. | filled `PROJECT_INSTRUCTIONS.md` |
| **Structure guide** | Explains where everything lives so the workspace stays tidy. | `PROJECT_STRUCTURE.md` |

> Always generate these. Everything below is conditional on the interview.

---

## 2. Modules (set up by need)

### `marketing/`
- **What:** strategy, campaigns and content memory — turns data into prioritized actions.
- **Trigger:** the user does any marketing / content / lead-gen.
- **If they run NO paid ads:** generate `strategy.md` in *organic* shape (channels, funnel, referral, content) and keep `campaigns.md` + `monitoraggio/` as **dormant stubs** — don't fill the CPC/budget/RSA scaffolding.
- **Creates:** `marketing/strategy.md`, `marketing/campaigns.md`, `marketing/content.md`, `marketing/monitoraggio/`.

### `website/`
- **What:** a living audit + backlog of the site (copy, SEO, UX, conversion).
- **Trigger:** the user has (or is building) a website.
- **Creates:** `website/website_notes.md`, `website/backlog.md`, `website/homepage_copy.md`.

### 🚩 `linkedin/` — LinkedIn Growth OS
- **What:** a full system to turn know-how into authority and leads on a personal/founder profile — strategy, a content engine (6 formats + hook/CTA banks), a reputation engine, an engagement playbook, and a runnable 8-step editor.
- **Trigger:** the user is the face of the brand / wants to grow a personal or founder profile on LinkedIn.
- **Creates:** the `linkedin/` folder, filled with their angle, pillars and cadence.
- **Pairs with automations:** `trend-hunter-linkedin`, `engagement-radar-daily`, `linkedin-connection-batch`.
- ⚠️ **Rewrite the worked examples.** The engagement playbook, reputation People-Map hints and calendar occasions carry **illustrative examples in the prose** (not just `{{placeholders}}`). For a non-AI / different-domain business, **replace every concrete example with one from the user's domain** (keyword searches, comment voice, the worked comment, role hints). Leaving foreign-domain examples in is a correctness bug.

### 🚩 `missions/` — Relentless Outcome Workflow
- **What:** "mission mode" — for an ambitious goal Claude pursues an *outcome*, not a task (route maps, evidence logs, stop conditions). E.g. landing a partnership, breaking into named accounts.
- **Trigger:** the user names a big, hard goal (a partnership, a dream client, an ecosystem to break into).
- **Creates:** a `missions/<slug>/` from the template + `workflows/relentless_outcome_workflow.md`.
- **Pairs with:** `mission-weekly-review`.

### `products/`
- **What:** a separate workstream per owned product (roadmap, validation, GTM), kept apart from marketing memory.
- **Trigger:** the user has one or more of their own products (not just client work).
- **Creates:** a `products/<name>/` from the template.

---

## 3. Scheduled automations (recurring — explain, then offer to set up)

> Most users don't know Claude can run on a schedule. Explain it simply: *"I can run this automatically every week and leave you a brief — want me to?"* Set up only the ones that match, with the suggested cadence (adjustable). Prompts live in `scheduled-tasks/`.

| Automation | Plain-language pitch | Trigger | Suggested cadence |
|---|---|---|---|
| **weekly-marketing-pulse** | A Monday brief on what your marketing did and the week's priorities. | does marketing | Mon 08:00 (`0 8 * * 1`) |
| **campaign-conversion-review** | Mid-week check on ad spend, conversions and what to fix. | runs paid ads | Wed 09:00 (`0 9 * * 3`) |
| **website-content-review** | Weekly look at site + content opportunities. | has a site/content | Fri 09:00 (`0 9 * * 5`) |
| **workspace-maintenance** | Keeps the knowledge base clean: de-dupes, resolves stale questions. | everyone | 1st & 15th 15:00 (`0 15 1,15 * *`) |
| **trend-hunter-linkedin** | Finds on-topic trends to post about, filtered to your category. | uses LinkedIn OS | Mon & Thu 07:30 (`30 7 * * 1,4`) |
| **engagement-radar-daily** | A daily list of in-target posts to comment on, in your voice (drafts only). | wants LinkedIn engagement | Mon–Fri 08:00 (`0 8 * * 1-5`) |
| **mission-weekly-review** | Weekly status + next routes for an active mission. | has a mission | Mon 08:30 (`30 8 * * 1`) |
| **linkedin-connection-batch** | Sends the queued, pre-approved connection requests. | does LinkedIn outreach | weekdays (`0 10 * * 1-5`) |
| **founder-weekly-review** | A Monday founder review across your CRM + workspace. | founder wants a weekly OS review | Mon 09:00 (`0 9 * * 1`) |
| **founder-daily-brief** | A short morning chief-of-staff brief: agenda + inbox/leads + mission urgencies (read-only). | founder wants a daily brief | weekdays 07:30 (`30 7 * * 1-5`) |

**Safety:** automations that touch the outside world (comments, connection requests, emails) **draft only** — nothing is sent without the user's approval. Say this out loud when proposing them.

**Connector check:** several routines only pay off if a connector is linked — `weekly-marketing-pulse` / `campaign-conversion-review` need analytics/ads; the LinkedIn routines need Chrome; `founder-weekly-review` needs a CRM; `founder-daily-brief` needs calendar/email. **Only propose a routine whose connector is actually connected** — otherwise offer to connect it, or a lighter alternative, rather than scheduling a run that comes back empty.

---

## 4. Skills (use if available; recommend if not)

> Skills are specialized capabilities Claude can invoke. The average user doesn't know they exist — surface them when relevant.

- **This kit's built-in "editor":** `linkedin/editor_workflow.md` works like a runnable LinkedIn editor ("esegui l'editor su [asset]") with no install. Mention it whenever the user wants to produce posts.
- **Named skills the user may already have** (use them if installed, otherwise tell the user they exist — see `skills/README.md`):
  - `document-data-extractor` → turning documents / invoices / receipts into a spreadsheet;
  - `validation-outreach` → cold messages to book discovery interviews;
  - `verification` → proving a technical task actually works before calling it done;
  - `youtube-transcript` → a YouTube link or a transcript request;
  - office builders `docx` / `pptx` / `xlsx` / `pdf` (and `html-presentations`) → a deliverable that should be a doc, deck, sheet or PDF;
  - `technical-decision-memory` → revisiting an architecture/tooling choice.
- **Rule:** if a relevant skill is installed, just use it. If it isn't, name it and point the user to where capabilities/plugins are managed — don't silently skip it.
- **Folder:** [`skills/README.md`](./skills/README.md) catalogs the skills that pair with cowork-os and is where the user keeps their own custom skills.

---

## 5. Mapping cheat-sheet (interview answer → propose)

- *"I'm the founder / the face of the brand"* → LinkedIn Growth OS + trend-hunter + engagement-radar.
- *"I run ads" (analytics/ads connected)* → marketing/ + weekly-marketing-pulse + campaign-conversion-review. *Organic-only* → marketing/ in organic shape + a lighter LinkedIn/content pulse; skip the ads routines.
- *"I have a website"* → website/ + website-content-review.
- *"I have my own product(s)"* → products/.
- *"I want to land [big partner / dream client]"* → missions/ + mission-weekly-review.
- *"I do outreach"* → linkedin-connection-batch and/or the validation-outreach skill.
- *"I want a morning brief / a chief-of-staff"* → founder-daily-brief.
- *"I have a pile of unsorted material"* → the `_inbox/` intake flow ("process the inbox").
- *Always* → Core + workspace-maintenance + the Memory Update habit.
