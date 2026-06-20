# Missions

**Outcome-driven missions for Claude Cowork — pursue a result, not a task.**
*Missioni orientate all'outcome per Claude Cowork — persegui un risultato, non un task.*

---

## EN — What missions are

A **mission** is an ambitious goal that won't be solved by a single prompt: landing a partnership, getting the first paying customers, opening a new channel. The default way people use an AI assistant — "write this email", "make that list" — stops the moment the email is sent. A mission doesn't.

This module packages the [**Relentless Outcome Workflow**](../workflows/relentless_outcome_workflow.md) into a copy-paste folder you fill in once per mission. The workflow is the method; this folder is where a specific mission lives.

The core shift:

> The mission is **not** "send an email to X". The mission is **make it inevitable that X has a reason to talk to you** — and keep finding routes until that's true.

### How a mission uses the workflow

Every mission follows the same five-part structure (full version in [`../workflows/relentless_outcome_workflow.md`](../workflows/relentless_outcome_workflow.md)):

1. **Mission** — the goal written as an *outcome*, not a task.
2. **Definition of Done** — the explicit conditions that close the mission.
3. **Route Map** — **at least 5 routes** to the outcome, mapped *before* acting.
4. **Route Execution Loop** — per route: hypothesis → action → asset → people → message → risk → probability → next step → result → alternative.
5. **Evidence Log** — every meaningful action recorded, so you never loop or re-try the same dead end.

Two guardrails the workflow makes non-negotiable:

- **Escalation** — the agent prepares (drafts, lists, plans); the human decides what gets sent. Every external message is approved before it goes out. No spam, no fake identities, no automated outreach without sign-off.
- **Stop Condition** — "impossible" can only be declared after a defined amount of real effort (routes explored, contacts mapped, messages prepared, workarounds tried). Until then, the mission has a road.

### How to start a mission

1. **Copy `_TEMPLATE/`** into a new folder named after the mission, e.g. `missions/partnership-001/` or `missions/first-enterprise-clients/`.
2. Open `mission.md` and write the **outcome** and **Definition of Done** first. If you can't state when it's *done*, it's not a mission yet.
3. Map **≥5 routes** in `route_map.md` before touching anyone. Breadth beats depth here.
4. Run the loop. Log every action in `mission_log.md` as you go.
5. Do a **Daily Mission Review** in `next_actions.md`: done · blocked · next · alternative route · what's needed from the human.
6. Update memory at the end of each session (see the OS-wide Memory Update protocol).

> Keep real third-party names, figures and private contacts **out** of these files if the repo is shared. Use the `{{PLACEHOLDERS}}` and keep sensitive content local.

---

## IT — Cosa sono le missioni

Una **missione** è un obiettivo ambizioso che non si risolve con un singolo prompt: chiudere una partnership, portare i primi clienti paganti, aprire un nuovo canale. Il modo in cui di solito si usa un assistente AI — "scrivi questa mail", "fammi quella lista" — si ferma nel momento in cui la mail parte. Una missione no.

Questo modulo pacchettizza il [**Relentless Outcome Workflow**](../workflows/relentless_outcome_workflow.md) in una cartella copia-incolla da compilare una volta per missione. Il workflow è il metodo; questa cartella è dove vive la singola missione.

Il cambio di prospettiva:

> La missione **non** è "mandare una mail a X". La missione è **rendere inevitabile che X abbia un motivo per parlarti** — e continuare a cercare strade finché non è vero.

### Come una missione usa il workflow

Ogni missione segue la stessa struttura in cinque parti (versione completa in [`../workflows/relentless_outcome_workflow.md`](../workflows/relentless_outcome_workflow.md)):

1. **Mission** — l'obiettivo scritto come *outcome*, non come task.
2. **Definition of Done** — le condizioni esplicite che chiudono la missione.
3. **Route Map** — **almeno 5 strade** verso l'outcome, mappate *prima* di agire.
4. **Route Execution Loop** — per ogni strada: ipotesi → azione → asset → persone → messaggio → rischio → probabilità → next step → risultato → alternativa.
5. **Evidence Log** — ogni azione rilevante registrata, così non entri mai in loop né ritenti lo stesso vicolo cieco.

Due guardrail resi non negoziabili dal workflow:

- **Escalation** — l'agente prepara (bozze, liste, piani); la persona decide cosa inviare. Ogni messaggio esterno viene approvato prima di partire. Niente spam, niente identità false, niente outreach automatico senza ok.
- **Stop Condition** — "impossibile" si può dichiarare solo dopo una quantità definita di lavoro reale (strade esplorate, contatti mappati, messaggi preparati, workaround tentati). Fino ad allora, la missione ha una strada.

### Come avviare una missione

1. **Copia `_TEMPLATE/`** in una nuova cartella col nome della missione, es. `missions/partnership-001/` o `missions/primi-clienti-enterprise/`.
2. Apri `mission.md` e scrivi prima l'**outcome** e la **Definition of Done**. Se non sai dire quando è *fatta*, non è ancora una missione.
3. Mappa **≥5 strade** in `route_map.md` prima di contattare chiunque. Qui l'ampiezza batte la profondità.
4. Esegui il loop. Registra ogni azione in `mission_log.md` mentre procedi.
5. Fai una **Daily Mission Review** in `next_actions.md`: fatto · bloccato · prossima · strada alternativa · cosa serve dalla persona.
6. Aggiorna la memoria a fine sessione (vedi il protocollo Memory Update dell'OS).

> Se il repo è condiviso, tieni **fuori** da questi file nomi di terzi reali, numeri e contatti privati. Usa i `{{PLACEHOLDER}}` e mantieni i contenuti sensibili in locale.

---

## Files in `_TEMPLATE/`

| File | What it holds |
|---|---|
| `mission.md` | Outcome, Definition of Done, route map summary, execution loop, evidence-log table, escalation, stop condition. |
| `route_map.md` | The ≥5 routes, each with hypothesis / action / asset / people / message / risk / probability / next step / alternative. |
| `next_actions.md` | Daily Mission Review: done · blocked · next · alternative route · what's needed. |
| `mission_log.md` | Evidence Log table: date · route · action · target · status · result · next step · notes. |
