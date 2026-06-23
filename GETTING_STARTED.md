# Getting started · Come iniziare

A 30-minute setup. *Setup in 30 minuti.*

---

## EN

### Path A — guided setup (recommended)
Copy the `cowork-os/` folder into a new Cowork project, paste the contents of [`INSTALL.md`](./INSTALL.md) into the chat, and answer ~6 questions. Claude builds and pre-configures the whole workspace for you — including the recurring automations that fit your business — and surfaces capabilities you may not know exist. Skip the rest of this page unless you'd rather do it by hand.

### Path B — manual setup

### 1. Get the files
Copy the `cowork-os/` folder into your Claude Cowork project folder (or clone the repo and point Cowork at it). Anything that works on Markdown files works here — there's nothing to install.

### 2. Configure once
Open [`cowork.config.example.md`](./cowork.config.example.md). It lists every `{{PLACEHOLDER}}` used across the templates (company name, one-liner, founder, website, ICP, services, category, KPIs…). Fill it in. Keep it as your single source of truth.

### 3. Install the operating rules
Open [`PROJECT_INSTRUCTIONS.md`](./PROJECT_INSTRUCTIONS.md), replace the placeholders with your values, and paste it into your Cowork project's **custom instructions**. This is what makes the agent check sources, separate facts from assumptions, and run a **Memory Update** at the end of every task.

### 4. Fill your context
Spend 20 minutes on `context/`:
- `overview.md` — what you do, your market, current state.
- `positioning.md` — value proposition, key messages, differentiation.
- `services.md` — your offers and use cases.
- `tone_of_voice.md` — words to use / avoid, good vs. bad copy.

Each file has a skeleton + a sanitized Yempik example to copy the shape from.

### 5. Work — and let it remember
Use the project normally. The rule that makes the whole thing compound: **end every important task with a Memory Update** (the format is in `PROJECT_INSTRUCTIONS.md`). Decisions go to `decisions/decisions_log.md`, open questions to `decisions/open_questions.md`, and so on.

### 6. Turn on the flagship modules (optional)
- **LinkedIn Growth OS** → see [`linkedin/README.md`](./linkedin/README.md).
- **Missions** → copy [`missions/_TEMPLATE/`](./missions/) and follow the [Relentless Outcome Workflow](./workflows/relentless_outcome_workflow.md).
- **Scheduled tasks** → see [`scheduled-tasks/README.md`](./scheduled-tasks/README.md) to recreate the recurring automations.

### Keep it healthy
Run a maintenance review every couple of weeks (`reviews/maintenance_review.TEMPLATE.md`): de-duplicate files, resolve stale open questions, fix naming drift.

---

## IT

### Via A — setup guidato (consigliato)
Copia la cartella `cowork-os/` in un progetto Cowork nuovo, incolla il contenuto di [`INSTALL.md`](./INSTALL.md) nella chat e rispondi a ~6 domande. Claude costruisce e pre-configura tutto il workspace per te — incluse le automazioni ricorrenti adatte al tuo business — e ti propone funzioni che forse non sai che esistono. Salta il resto di questa pagina, a meno che tu non preferisca farlo a mano.

### Via B — setup manuale

### 1. Prendi i file
Copia la cartella `cowork-os/` dentro la cartella del tuo progetto Claude Cowork (o clona il repo e punta Cowork lì). Tutto ciò che lavora su file Markdown funziona qui — non c'è niente da installare.

### 2. Configura una volta
Apri [`cowork.config.example.md`](./cowork.config.example.md). Elenca ogni `{{PLACEHOLDER}}` usato nei template (nome azienda, one-liner, founder, sito, ICP, servizi, categoria, KPI…). Compilalo. Tienilo come unica fonte di verità.

### 3. Installa il cervello
Apri [`PROJECT_INSTRUCTIONS.md`](./PROJECT_INSTRUCTIONS.md), sostituisci i placeholder con i tuoi valori e incollalo nelle **istruzioni personalizzate** del tuo progetto Cowork. È ciò che fa controllare le fonti all'agente, separare fatti e ipotesi, e fare una **Memory Update** a fine di ogni task.

### 4. Compila il contesto
Dedica 20 minuti a `context/`:
- `overview.md` — cosa fai, il tuo mercato, lo stato attuale.
- `positioning.md` — proposta di valore, messaggi chiave, differenziazione.
- `services.md` — offerte e use case.
- `tone_of_voice.md` — parole da usare / evitare, copy buono vs. da evitare.

Ogni file ha uno scheletro + un esempio Yempik sanitizzato da cui copiare la forma.

### 5. Lavora — e lascia che ricordi
Usa il progetto normalmente. La regola che fa accumulare valore: **chiudi ogni task importante con una Memory Update** (il formato è in `PROJECT_INSTRUCTIONS.md`). Le decisioni vanno in `decisions/decisions_log.md`, le domande aperte in `decisions/open_questions.md`, e così via.

### 6. Attiva i moduli faro (opzionale)
- **LinkedIn Growth OS** → vedi [`linkedin/README.md`](./linkedin/README.md).
- **Missions** → copia [`missions/_TEMPLATE/`](./missions/) e segui il [Relentless Outcome Workflow](./workflows/relentless_outcome_workflow.md).
- **Scheduled tasks** → vedi [`scheduled-tasks/README.md`](./scheduled-tasks/README.md) per ricreare le automazioni ricorrenti.

### Tienilo in salute
Fai una review di manutenzione ogni due settimane (`reviews/maintenance_review.TEMPLATE.md`): deduplica i file, chiudi le domande aperte stantie, sistema le derive di naming.
