# LinkedIn Growth OS

> A reusable, opinionated operating system for growing a **founder / personal brand** on LinkedIn — built for operators, not creators. Part of **cowork-os**, an open-source Claude Cowork starter kit.
>
> Authored by **Yempik** (a software house) and used here as the sanctioned example. Copy it, fill in the `{{placeholders}}`, and run it inside your own Claude Cowork project.

---

## EN — What this is

This module turns the know-how a company already has into LinkedIn authority, quality conversations, and commercial opportunities. The engine is a **personal profile** (not a company page), and it optimizes for **impressions, comments, profile visits, and leads — never likes**.

It is not a content calendar with extra steps. It is a machine: principles → strategy → production method → distribution → measurement → improvement. Three pillars work together:

1. **Content engine** — *what* you publish (extraction, formats, templates, idea bank).
2. **Reputation engine** — *which mental category* you come to own (Category Thesis, Reputation Score, Association Test).
3. **Engagement playbook** — *how you get target decision-makers into your comments* (engage-first, warming, first 60 minutes).

The whole system is designed to be operated together with Claude inside Cowork: you point Claude at a source asset, and it runs the **personal editor** workflow to turn it into ready-to-publish posts.

### Who it is for

Operators with real implementations, real clients, real mistakes — people whose competitive advantage is *experience*, not communication. If you build things and want the right people to know it, this is for you. If you want vanity metrics, this is the wrong tool.

### How to start (5 steps)

1. **Read `strategy.md`** and fill in the placeholders: `{{ICP}}`, your positioning angle, the 4 content pillars, cadence, KPIs.
2. **Set the Category Thesis** in `reputation_engine.md` — the single idea you want to own.
3. **Fill the idea bank** in `content_engine.md` by running the editor on 2-3 of your real assets (an article, a case study, a deck).
4. **Pick the warming list** in `engagement_playbook.md` — the real connections you already have in target.
5. **Run the editor:** tell Claude *"esegui l'editor su [asset]"* and publish your first post. Log it in `post_tracker.md`.

> First non-negotiable: you optimize for **conversations and leads**, not likes. Even 1-2 quality conversations a month is ROI.

---

## IT — Cos'è

> **EN —** Module landing page: the LinkedIn Growth OS, its three pillars, and how to start. Update when the file structure or the three-pillar model changes.
> **IT —** Pagina di apertura del modulo: il LinkedIn Growth OS, i suoi tre pilastri e come iniziare. Aggiornare quando cambiano la struttura dei file o il modello a tre pilastri.

Questo modulo è il **sistema operativo** per la crescita del profilo personale di un founder su LinkedIn: trasformare il know-how già presente in `{{COMPANY}}` in **autorevolezza, conversazioni di qualità e opportunità commerciali**. Il motore è il **profilo personale** (`{{FOUNDER}}`), non la pagina aziendale, e si ottimizza per **impression, commenti, profili visitati e lead — mai per i like**.

Non è una raccolta di post. È una macchina: principi → strategia → metodo di produzione → distribuzione → misurazione → miglioramento.

### I tre pilastri

| Pilastro | File | Risponde a |
|----------|------|------------|
| **Content engine** | `content_engine.md` | *Cosa* pubblichi |
| **Reputation engine** | `reputation_engine.md` | *Quale categoria mentale* possiedi |
| **Engagement playbook** | `engagement_playbook.md` | *Come* fai entrare i decisori in target nei tuoi commenti |

Senza il terzo, i post non bastano: il contenuto ti fa *trovare*, la relazione fa *commentare* i decisori.

### I file del modulo

| File | Contiene | Modificabile |
|------|----------|--------------|
| `README.md` | Questa pagina: panoramica, tre pilastri, come iniziare | Sì, evolve |
| `strategy.md` | Strategia: audience/ICP, angolo founder, 4 pillar, cadenza, KPI, roadmap 90gg | Sì, evolve |
| `content_engine.md` | Metodo di produzione + idea bank + template + hook/CTA bank | Sì, continuo |
| `reputation_engine.md` | Category Thesis, Theme/Format, Reputation Score, Association Test, People Map, Trend Hunter, Comment Mining, KPI Hierarchy | Sì, continuo |
| `engagement_playbook.md` | Distribuzione relazionale: engage-first, Engagement Radar, warming, primi 60', DM non-pitch, "Dream 30" | Sì, continuo |
| `editor_workflow.md` | Il workflow "editor personale" runnable (8 step) | Sì, evolve |
| `calendar.md` | Calendario editoriale 3/sett e rotazione Theme | Sì, settimanale |
| `post_tracker.md` | Registro performance dei post + review pattern mensile | Sì, continuo |
| `trend_hunter/` | Routine settimanale automatizzata: segnali AI → idee post | Append |
| `engagement_radar/` | Digest giornaliero: dove trovare post in target da commentare | Append |
| `research/` | Benchmark esterni datati con fonti | Append |

**Regola anti-duplicazione:** una sola fonte per informazione. I principi stanno nella strategia; voce e posizionamento in `../context/` (se presente nel tuo Project); strategia, metodo e dati operativi qui.

### Principi non negoziabili

1. `{{FOUNDER}}` è un **operatore**, non un creator: si distribuisce esperienza reale.
2. Un **articolo** dimostra una tesi; un **post** ne vende una. **Una sola tesi per post.**
3. L'**hook** (prime 2 righe) crea **tensione**, non spiega.
4. Si ottimizza per **impression, commenti, profili visitati, lead** — mai per like.
5. Non si inventano idee nuove: si **distribuisce meglio** il know-how `{{COMPANY}}` esistente.

### Da dove partire

1. `strategy.md` — la direzione: audience, angolo, pillar, cadenza, KPI, roadmap 90gg.
2. `content_engine.md` — come si produce un post (extraction → 6 format → checklist → idea bank → template → hook/CTA bank).
3. `reputation_engine.md` — come ogni contenuto costruisce la categoria mentale `{{CATEGORY}}` → `{{FOUNDER}}`.
4. `engagement_playbook.md` — come far interagire i decisori in target.
5. `editor_workflow.md` — il workflow runnable. Si invoca con *"esegui l'editor su [asset]"*.
6. `calendar.md` + `post_tracker.md` — ritmo settimanale e misurazione.

### Il motore di produzione (come nasce un post)

```
Asset {{COMPANY}} (articolo, caso, deck, storia, bozza)
   → content extraction (≥10-20 idee)  →  idea bank (content_engine.md)
   → editor 8 step  →  post pronto (hook A/B, corpo, CTA, link nel 1° commento)
   → pubblica + presidia 60'  →  registra nel post_tracker.md
   → review pattern mensile  →  doppia su ciò che funziona
```

> Un esempio compilato e sanitizzato di questo modulo vive in `examples/yempik/linkedin/` (Yempik come azienda di riferimento).
