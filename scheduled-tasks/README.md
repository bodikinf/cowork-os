# Scheduled tasks

> A library of ready-to-use **recurring automations** for Claude Cowork — prompt templates you schedule once and let run on their own. Part of **cowork-os**, an open-source Claude Cowork starter kit. Authored by **Yempik** (es. `{{COMPANY}}` = Yempik) and used here as the sanctioned example.

---

## EN — What this is

A **scheduled task** is a prompt that Claude Cowork runs automatically on a cadence you set — every Monday at 08:00, the 1st and 15th of the month, weekday mornings, and so on. Instead of remembering to run your weekly marketing review or your LinkedIn engagement scan, you wire it up once and the agent does it for you, reading from and writing back to your `cowork-os` memory files.

This module ships **10 task templates**. Each one is a self-contained Markdown file with:

- a **bilingual one-line header** (what it does + suggested cadence),
- a **suggested cron schedule**, and
- the **prompt body** (in Italian, with `{{placeholders}}` you fill in).

They are templates: replace `{{COMPANY}}`, `{{FOUNDER}}`, `{{WEBSITE}}`, `{{MISSION}}`, etc. with your own values (see [`../cowork.config.example.md`](../cowork.config.example.md)), then schedule the ones you want. Nothing here sends an email, a DM, or a connection request without your explicit approval — the outreach tasks are **draft-only or propose-only** by design.

### How to recreate one in Claude Cowork

You don't need a YAML file or a config UI. There are two easy ways:

**1. Just ask, in plain language.** Tell Claude the cadence and what to do, and it will create the scheduled task for you. For example:

> *"Ogni lunedì alle 8 esegui il weekly marketing pulse."*
> *"Il 1 e il 15 di ogni mese, alle 15, fai la workspace maintenance."*
> *"Ogni mattina nei giorni feriali, alle 8, lancia l'engagement radar."*

Claude will confirm the schedule and save it. You can change or cancel it any time (*"sposta il pulse a martedì"*, *"ferma il trend hunter"*).

**2. Paste the prompt body.** Open the task file you want, copy everything under **Prompt:**, fill in the `{{placeholders}}`, and either paste it into a new scheduled task or save it as a reusable prompt. Use the **suggested cron** next to it (or the human cadence in the header) to pick the timing.

> Tip: start with **one** task — the *weekly marketing pulse* is the best first one — see it run once, then add the others. Each task ends with a `Memory Update` (or writes a dated file), so the rest of your `cowork-os` stays in sync automatically.

### Before you schedule

- Fill the placeholders for that task (company, founder, website, mission, keywords…).
- Make sure the **connectors** the task needs are linked in your Cowork project: analytics/ads (e.g. Supermetrics, Google Ads, GA4) for the marketing tasks, **Claude in Chrome** for the LinkedIn tasks, and your **CRM** for the founder review.
- Keep the safety rails: the LinkedIn and outreach tasks are deliberately **read-only / draft-only**. Don't remove the "non inviare nulla senza approvazione" lines.

---

## IT — Cosa sono

> **EN —** Module landing page: what scheduled tasks are, how to recreate each one in Cowork, and the table of the 10 tasks. Update when a task is added, removed, or its cadence changes.
> **IT —** Pagina di apertura del modulo: cosa sono gli scheduled task, come ricrearli in Cowork e la tabella dei 10 task. Aggiornare quando un task viene aggiunto, rimosso o cambia cadenza.

Un **task pianificato** è un prompt che Claude Cowork esegue automaticamente con la cadenza che imposti tu — ogni lunedì alle 08:00, il 1 e il 15 del mese, le mattine feriali, e così via. Invece di ricordarti di lanciare la review marketing o lo scan di engagement su LinkedIn, lo configuri una volta e l'agente lo fa al posto tuo, leggendo e riscrivendo i tuoi file di memoria `cowork-os`.

Questo modulo include **10 template di task**. Ogni file Markdown è autonomo e contiene:

- un **header bilingue di una riga** (cosa fa + cadenza suggerita),
- una **cron suggerita**, e
- il **corpo del prompt** (in italiano, con i `{{placeholders}}` da compilare).

Sono template: sostituisci `{{COMPANY}}`, `{{FOUNDER}}`, `{{WEBSITE}}`, `{{MISSION}}`, ecc. con i tuoi valori (vedi [`../cowork.config.example.md`](../cowork.config.example.md)), poi pianifica quelli che ti servono. Nessun task qui invia email, DM o richieste di collegamento senza la tua approvazione esplicita — i task di outreach sono **draft-only o propose-only** per scelta.

### Come ricrearne uno in Claude Cowork

Non serve un file YAML o una UI di configurazione. Due modi semplici:

**1. Chiedilo a voce.** Di' a Claude la cadenza e cosa fare: creerà il task pianificato per te. Per esempio:

> *"Ogni lunedì alle 8 esegui il weekly marketing pulse."*
> *"Il 1 e il 15 di ogni mese, alle 15, fai la workspace maintenance."*
> *"Ogni mattina nei giorni feriali, alle 8, lancia l'engagement radar."*

Claude conferma la pianificazione e la salva. Puoi modificarla o annullarla quando vuoi (*"sposta il pulse a martedì"*, *"ferma il trend hunter"*).

**2. Incolla il corpo del prompt.** Apri il file del task che vuoi, copia tutto ciò che sta sotto **Prompt:**, compila i `{{placeholders}}` e incollalo in un nuovo task pianificato (o salvalo come prompt riutilizzabile). Usa la **cron suggerita** accanto (o la cadenza in chiaro nell'header) per scegliere l'orario.

> Consiglio: parti da **un solo** task — il *weekly marketing pulse* è il migliore per iniziare — guardalo girare una volta, poi aggiungi gli altri. Ogni task chiude con un `Memory Update` (o scrive un file datato), così il resto del tuo `cowork-os` resta allineato in automatico.

### Prima di pianificare

- Compila i placeholder di quel task (azienda, founder, sito, missione, keyword…).
- Assicurati che i **connettori** richiesti siano collegati nel tuo progetto Cowork: analytics/ads (es. Supermetrics, Google Ads, GA4) per i task marketing, **Claude in Chrome** per i task LinkedIn, e il tuo **CRM** per la founder review.
- Mantieni i paletti di sicurezza: i task LinkedIn e di outreach sono volutamente **solo lettura / draft-only**. Non rimuovere le righe "non inviare nulla senza approvazione".

---

## The 10 tasks / I 10 task

| # | Task file | Suggested cron | Cadence | What it does (one line) |
|---|-----------|----------------|---------|--------------------------|
| 1 | [`weekly-marketing-pulse.md`](./weekly-marketing-pulse.md) | `0 8 * * 1` | Mon 08:00 | Weekly read of analytics + ad campaigns + marketing/website memory → the week's priorities + 5 actions. |
| 2 | [`campaign-conversion-review.md`](./campaign-conversion-review.md) | `0 9 * * 3` | Wed 09:00 | Checks if paid campaigns generate useful signals; proposes campaign/keyword/landing optimizations (proposes, never edits the account). |
| 3 | [`website-content-review.md`](./website-content-review.md) | `0 9 * * 5` | Fri 09:00 | Keeps site + content + messaging coherent with positioning; turns ideas into concrete backlog tasks. |
| 4 | [`workspace-maintenance.md`](./workspace-maintenance.md) | `0 15 1,15 * *` | 1st & 15th, 15:00 | Audits the knowledge base for unsaved decisions, duplicates, stale info and conflicts (never deletes history). |
| 5 | [`trend-hunter-linkedin.md`](./trend-hunter-linkedin.md) | `0 7 * * 1,4` | Mon (full) + Thu (pulse) | Scans web/RSS + X through your Category Thesis → emerging trends + post ideas, with a strict read-budget cap. |
| 6 | [`engagement-radar-daily.md`](./engagement-radar-daily.md) | `0 8 * * 1-5` | Weekdays 08:00 | Opens Chrome on LinkedIn, finds on-target posts to comment on → link + recap + angle in your voice (read-only). |
| 7 | [`mission-weekly-review.md`](./mission-weekly-review.md) | `30 8 * * 1` | Mon 08:30 | Reconstructs your active mission's state, checks accepted connections + news, updates next actions, reports only decisions you owe. |
| 8 | [`linkedin-connection-batch.md`](./linkedin-connection-batch.md) | `0 10 * * 1` | Weekly (Mon 10:00) | Works the outreach queue and sends pending LinkedIn connection requests (personalized note each); never pitch DMs. |
| 9 | [`founder-weekly-review.md`](./founder-weekly-review.md) | `0 9 * * 1` | Mon 09:00 | Reads your live CRM pipeline + Startup OS → this week's ready-to-run agenda to move a deal forward (draft-only). |
| 10 | [`founder-daily-brief.md`](./founder-daily-brief.md) | `30 7 * * 1-5` | Weekdays 07:30 | Morning chief-of-staff brief: today's agenda + inbox/leads to handle + mission urgencies, in one short read (read-only). |

> Cron format is `minute hour day-of-month month day-of-week`. Day-of-week: `1` = Monday … `7` = Sunday. Adjust to your timezone and rhythm — the cadences above are suggestions, not rules.
>
> Formato cron: `minuto ora giorno-del-mese mese giorno-della-settimana`. Giorno della settimana: `1` = lunedì … `7` = domenica. Adatta al tuo fuso e al tuo ritmo — le cadenze sopra sono suggerimenti, non regole.
