# Signals

> **EN —** The **ingestion layer** of cowork-os. Scheduled sweeps read your real communication (email sent + received, Slack) and distill it into structured *signals* — decisions made, commitments, questions, risks, deadlines — that feed the **Decision Radar**. Raw signal dumps are private and never committed. Part of **cowork-os**, an open-source Claude Cowork starter kit by **Yempik**.
> **IT —** Il **layer di ingestione** di cowork-os. Gli sweep schedulati leggono la tua comunicazione reale (email inviate + ricevute, Slack) e la distillano in *signal* strutturati — decisioni prese, impegni, domande, rischi, scadenze — che alimentano il **Decision Radar**. I dump grezzi sono privati e non vengono mai committati.

---

## The three layers · I tre layer

cowork-os separa tre lavori che spesso vengono confusi:

| Layer | File / task | Job | Cadenza |
|---|---|---|---|
| **1. Ingestione** | `signals/` + `daily-signal-sweep-am/pm` | Legge email/Slack → estrae signal → propone **decision candidates** | 2×/giorno |
| **2. Governance** | `decisions/` + `decision-radar` | Legge le decisioni → cosa è attivo, scaduto, in conflitto, da decidere | settimanale |
| **3. Igiene** | `workspace-maintenance` | Tiene ordinato il KB: duplicati, file vuoti, archiviazione | 1 e 15 del mese |

> **Perché sono distinti.** `workspace-maintenance` sistema **solo file già dentro il workspace**: non legge email né Slack. Il signal-sweep è il pezzo mancante che **fa entrare** i dati esterni. Il Decision Radar li **governa**. Senza il layer 1, il Radar può ragionare solo su ciò che hai scritto a mano.

## Cosa fa lo sweep (in breve)

```
email (inviate + ricevute) + Slack
        │  legge SOLO dal watermark in sync-state.md (niente doppioni)
        ▼
  estrazione signal  →  signals/email/AAAA-MM-GG.md
                        signals/slack/AAAA-MM-GG.md
        │  i signal che sembrano DECISIONI/IMPEGNI
        ▼
  decisions/decision_candidates.md   (in attesa di conferma umana)
        │  conferma in Decision Radar
        ▼
  decisions/active_decisions.md  +  decisions_log.md
```

## Cosa è un "signal"

Un fatto atomico estratto dalla comunicazione, con **fonte** e **data**. Tipi:

- `decision` — è stata presa una scelta ("andiamo con il pricing a 4.500€").
- `commitment` — qualcuno si è impegnato a fare qualcosa entro una data.
- `question` — è emersa una domanda aperta / un dubbio non risolto.
- `risk` — un rischio o un blocco segnalato.
- `deadline` — una data che conta.
- `change` — un cambio rispetto a qualcosa deciso prima (possibile conflitto).

Solo `decision` e `commitment` diventano **candidate** in `decisions/decision_candidates.md`. Gli altri vanno in `signals/…` e, se rilevanti, in `open_questions.md` (question/risk).

## Privacy · Privacy

- **`signals/email/`, `signals/slack/`, `signals/notion/` e `signals/drive/` contengono contenuti privati** (estratti reali di email, messaggi e documenti). Sono in `.gitignore`: **non vengono mai committati**. Restano solo nella tua copia locale/privata.
- Ciò che è tracciato pubblicamente è solo: questo README, la struttura, e `sync-state.md` (che contiene **solo watermark** — timestamp/ID, nessun contenuto).
- Gli sweep sono **read-only**: leggono e scrivono file locali, **non inviano nulla** (né email, né messaggi, né bozze verso l'esterno).

## File del modulo

| File | Contiene | Tracciato |
|---|---|---|
| `README.md` | Questa pagina | Sì |
| `sync-state.md` | Watermark per fonte (ultimo elemento processato) → idempotenza | Sì (solo ID/timestamp) |
| `email/AAAA-MM-GG.md` | Signal estratti dalle email del giorno | **No** (gitignored) |
| `slack/AAAA-MM-GG.md` | Signal estratti da Slack del giorno | **No** (gitignored) |
| `notion/AAAA-MM-GG.md` | Modifiche a pagine/DB Notion osservati (signal `change`) | **No** (gitignored) |
| `drive/AAAA-MM-GG.md` | Modifiche a file nelle cartelle Drive osservate (signal `change`) | **No** (gitignored) |

## Connettori richiesti

- **Email** (es. Gmail): per leggere inviate + ricevute. *Verifica che sia collegato nel tuo progetto.*
- **Slack** *(lettura)*: un connettore Slack con accesso a messaggi e canali — trattalo come fonte piena, al pari dell'email (ricerca messaggi, thread, canali osservati).
- **Notion** *(lettura, opzionale)*: per rilevare modifiche alle pagine/DB in `pages_watched`. Change-detection via `last_edited_time` > watermark. Serve indicare quali pagine osservare, non tutto Notion.
- **Google Drive** *(lettura, opzionale)*: per rilevare file creati/modificati nelle `folders_watched`. Change-detection via `modifiedTime` > watermark.

> Se un connettore non è ancora collegato, lo sweep **non fallisce**: elabora le fonti disponibili e scrive una riga "fonte non disponibile" nel file del giorno, senza inventare. Notion e Drive sono **opzionali**: se assenti, lo sweep resta su email+Slack.
