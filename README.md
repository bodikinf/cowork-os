<div align="center">

<img src="docs/banner.png" alt="cowork-os: give your Claude Cowork project a memory you can read and edit" width="100%" />

# cowork-os

**Give your Claude Cowork project a memory you can read and edit.**
*Dai al tuo progetto Claude Cowork una memoria che puoi leggere e correggere.*

<sub>Open-source, MIT. An operating system in the boring sense: folder conventions and a memory protocol, not a kernel.</sub>

[![License: MIT](https://img.shields.io/badge/License-MIT-E35B2D.svg?style=flat-square)](./LICENSE)
&nbsp;![Made by Yempik](https://img.shields.io/badge/made%20by-Yempik-0A0A0A.svg?style=flat-square)
&nbsp;![For Claude Cowork](https://img.shields.io/badge/for-Claude%20Cowork-E35B2D.svg?style=flat-square)
&nbsp;![PRs welcome](https://img.shields.io/badge/PRs-welcome-0A0A0A.svg?style=flat-square)

Folder conventions · a living-memory protocol · outcome-driven workflows ·
and three flagship modules (LinkedIn Growth OS, Missions, Scheduled tasks).

Built and battle-tested by [**Yempik**](https://yempik.com) · maintained by Raffaele.

<br />

<img src="docs/demo.gif" alt="cowork-os installer in action: paste a file, answer 6 questions, get a configured workspace" width="540" />

_Paste the installer, answer 6 questions, and Claude builds your workspace._

</div>

---

## EN: What this is

Most people use AI chat as a disposable conversation: ask, get an answer, lose the context. **cowork-os** treats your Claude Cowork project as a **company workspace with a memory**. Every task reads from and writes back to a structured set of Markdown files, so the system gets *smarter every week* instead of forgetting everything.

It's not an app and it has no dependencies. It's a **folder structure + a set of prompts and conventions** you copy into a Cowork project (or any agentic-coding workspace) and adapt to your business in ~30 minutes.

<div align="center">
<img src="docs/chat-vs-memoria.png" alt="Disposable chat vs. a workspace with memory" width="460" />
</div>

### What's inside

| Layer | What it gives you |
|---|---|
| **Core OS** | A clean folder structure (`context/`, `marketing/`, `website/`, `decisions/`, `reviews/`) and the **Memory Update** protocol that keeps it alive. |
| **Project Instructions** | The system prompt that turns a generic assistant into a strategist that always checks sources, separates facts from assumptions, and updates memory. |
| **Relentless Outcome Workflow** | A method for *ambitious missions*: pursue an outcome, not a task. Route maps, evidence logs, stop conditions. |
| 🚩 **LinkedIn Growth OS** | A full system to turn know-how into authority and leads: strategy, a content engine (6 formats + hook/CTA banks), a reputation engine, an engagement playbook, and a runnable 8-step editor. |
| 🚩 **Missions** | The outcome framework, packaged as a copy-paste mission template. |
| 🚩 **Scheduled tasks** | 10 ready-to-use recurring automations (weekly marketing pulse, campaign review, workspace maintenance, trend hunter, engagement radar, mission review, daily founder brief…) as prompt templates + a setup guide. |

### Why it works

- **Living memory, not chat history.** Decisions, assumptions and open questions live in files, not in a thread that scrolls away.
- **Evidence over vibes.** The instructions force the agent to check real data and label facts vs. assumptions vs. recommendations.
- **Outcome over output.** The mission workflow refuses to stop at "I sent the email."
- **Adopt in 30 minutes.** Copy the folder, paste the Project Instructions, fill the placeholders. See [`GETTING_STARTED.md`](./GETTING_STARTED.md).

### Quick start, three ways

**🟢 Path A, one command (plugin, fastest).** On Claude Cowork or Code, add the marketplace and install the plugin:

```
/plugin marketplace add yempik-ai/cowork-os
/plugin install cowork-os@cowork-os
```

Then run `/cowork-os:install`: Claude interviews you (about 5 minutes) and **generates your whole workspace, pre-configured**, with no copy-paste and no files to understand.

**Path B, guided setup.** No plugin support? Copy the folder into a new Cowork project, paste the contents of [`INSTALL.md`](./INSTALL.md) into the chat, and answer ~6 questions. Same result. It even surfaces capabilities most people don't know exist (scheduled automations, mission mode, skills). Already have notes, a deck, or a messy folder? Drop it in `_inbox/` and Claude organizes it into the workspace for you.

**Path C, manual.** Prefer to do it by hand, or not on Cowork? Fill [`PROJECT_INSTRUCTIONS.md`](./PROJECT_INSTRUCTIONS.md) and the `context/` templates yourself, see [`GETTING_STARTED.md`](./GETTING_STARTED.md). Every file ships as a skeleton **plus a sanitized Yempik example**.

Then just work, and end important tasks with a **Memory Update** so the system gets smarter every week.

---

## IT: Cos'è

La maggior parte delle persone usa la chat AI come una conversazione usa-e-getta: chiedi, ottieni una risposta, perdi il contesto. **cowork-os** tratta il tuo progetto Claude Cowork come un **workspace aziendale con una memoria**. Ogni task legge e riscrive un set strutturato di file Markdown: così il sistema diventa *più intelligente ogni settimana* invece di dimenticare tutto.

Non è un'app e non ha dipendenze. È una **struttura di cartelle + un set di prompt e convenzioni** che copi dentro un progetto Cowork (o qualsiasi workspace agentico) e adatti alla tua azienda in ~30 minuti.

### Cosa c'è dentro

| Livello | Cosa ti dà |
|---|---|
| **Core OS** | Una struttura di cartelle pulita (`context/`, `marketing/`, `website/`, `decisions/`, `reviews/`) e il protocollo **Memory Update** che la tiene viva. |
| **Project Instructions** | Il system prompt che trasforma un assistente generico in uno strategist che controlla sempre le fonti, separa fatti e ipotesi, e aggiorna la memoria. |
| **Relentless Outcome Workflow** | Un metodo per le *missioni ambiziose*: persegui un outcome, non un task. Route map, evidence log, stop condition. |
| 🚩 **LinkedIn Growth OS** | Un sistema completo per trasformare know-how in autorevolezza e lead: strategia, content engine (6 format + hook/CTA bank), reputation engine, engagement playbook, editor a 8 step. |
| 🚩 **Missions** | Il framework outcome, pacchettizzato come template di missione copia-incolla. |
| 🚩 **Scheduled tasks** | 10 automazioni ricorrenti pronte all'uso (pulse marketing, review campagne, manutenzione workspace, trend hunter, engagement radar, review missioni, brief founder giornaliero…) come template di prompt + guida. |

### Perché funziona

- **Memoria viva, non cronologia chat.** Decisioni, ipotesi e domande aperte vivono nei file, non in un thread che scorre via.
- **Evidenze, non sensazioni.** Le istruzioni obbligano l'agente a controllare dati reali e a etichettare fatti / ipotesi / raccomandazioni.
- **Outcome, non output.** Il workflow delle missioni si rifiuta di fermarsi a "ho mandato la mail".
- **Adozione in 30 minuti.** Copia la cartella, incolla le Project Instructions, compila i placeholder. Vedi [`GETTING_STARTED.md`](./GETTING_STARTED.md).

### Avvio rapido, tre modi

**🟢 Via A, un comando (plugin, il più veloce).** Su Claude Cowork o Code, aggiungi il marketplace e installa il plugin:

```
/plugin marketplace add yempik-ai/cowork-os
/plugin install cowork-os@cowork-os
```

Poi lancia `/cowork-os:install`: Claude ti intervista (circa 5 minuti) e **genera tutto il workspace già configurato**, senza copia-incolla e senza file da capire.

**Via B, setup guidato.** Niente plugin? Copia la cartella in un progetto Cowork nuovo, incolla il contenuto di [`INSTALL.md`](./INSTALL.md) nella chat e rispondi a ~6 domande. Stesso risultato. Ti propone anche funzioni che quasi nessuno sa che esistono (automazioni schedulate, mission mode, skill). Hai già note, un deck o una cartella disordinata? Buttala in `_inbox/` e Claude la organizza nel workspace per te.

**Via C, manuale.** Preferisci farlo a mano, o non sei su Cowork? Compila tu [`PROJECT_INSTRUCTIONS.md`](./PROJECT_INSTRUCTIONS.md) e i template in `context/`, vedi [`GETTING_STARTED.md`](./GETTING_STARTED.md). Ogni file è uno scheletro **più un esempio Yempik sanitizzato**.

Poi lavora e basta, e chiudi i task importanti con una **Memory Update**, così il sistema diventa più intelligente ogni settimana.

---

## Structure / Struttura

```
cowork-os/
├── INSTALL.md                   # 🟢 guided setup, paste this, answer questions, done
├── capabilities.md              # what Claude can set up for you (the installer's "brain")
├── PROJECT_INSTRUCTIONS.md      # the system prompt (auto-filled by the installer, or by hand)
├── PROJECT_STRUCTURE.md         # how the knowledge base is organized
├── cowork.config.example.md     # every placeholder, in one place
├── GETTING_STARTED.md           # setup, both paths (EN + IT)
├── CONTRIBUTING.md
├── workflows/                   # Relentless Outcome Workflow
├── context/                     # overview · positioning · services · tone of voice
├── marketing/                   # strategy · campaigns · content
├── website/                     # notes · backlog · homepage copy
├── decisions/                   # decisions log · open questions
├── reviews/                     # weekly + maintenance review templates
├── missions/                    # 🚩 outcome-driven mission template
├── products/                    # product-workstream pattern
├── linkedin/                    # 🚩 LinkedIn Growth OS
├── scheduled-tasks/             # 🚩 recurring automations ("routines") + setup guide
├── skills/                      # skills that pair with the kit + your own
├── _inbox/                      # drop unsorted material → "process the inbox"
└── examples/yempik/             # 🟢 a complete, sanitized, real workspace
```

## License

[MIT](./LICENSE) © 2026 Yempik Ltd. Use it, fork it, ship it. A credit back to Yempik is appreciated, not required.

## Credits

Created by **Yempik**, a software house specialized in software, automation and AI agents, maintained by Raffaele. If this helped you, a star ⭐ and a tag on LinkedIn make our day.
