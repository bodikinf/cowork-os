> **EN —** How the knowledge base is organized and how to keep it tidy. Read this before adding files. The golden rule: don't duplicate; pick the most specific file.
> **IT —** Come è organizzata la knowledge base e come tenerla in ordine. Leggilo prima di aggiungere file. Regola d'oro: non duplicare; scegli il file più specifico.

---

# Project Structure

Quando lavori, usa questa struttura per leggere e aggiornare le informazioni.

Non duplicare contenuti tra file diversi. Se un'informazione potrebbe stare in più posti, scegli il file più specifico. Se non sei sicuro, aggiungila prima in `decisions/open_questions.md` o segnala il dubbio.

---

## Root

- `PROJECT_INSTRUCTIONS.md` — il system prompt del Project (tono, obiettivi, vincoli, Memory Update). In Cowork vive nelle istruzioni del progetto; qui lo teniamo come file versionabile.
- `PROJECT_STRUCTURE.md` — questo file. Aggiornalo solo quando aggiungi, rimuovi o rinomini cartelle.
- `cowork.config.example.md` — glossario dei placeholder.

## `context/`

Informazioni fondamentali e relativamente stabili.

- `overview.md` — descrizione generale, cosa fa l'azienda, visione, mercato, stato attuale. Non usarlo per task temporanei o note settimanali.
- `positioning.md` — posizionamento, proposta di valore, messaggi chiave, differenziazione, categorie di mercato, problemi risolti.
- `services.md` — servizi offerti, descrizione, priorità, pacchetti, use case.
- `tone_of_voice.md` — tono di voce, parole da usare/evitare, esempi di copy buono e da evitare.
- `processes/` — come si eseguono **davvero** i processi operativi (uno per file), catturati con la skill `knowledge-transfer`: passi reali, punti di decisione, eccezioni, regole non scritte. È il **layer operativo** del company brain (il "come si lavora", non solo il "chi siamo"). Le regole estratte vanno anche in `decisions/decisions_log.md` con la fonte-intervista. `_TEMPLATE.md` è lo stampo.

## `marketing/`

Strategia, campagne, contenuti e insight.

- `strategy.md` — strategia generale, obiettivi trimestrali, canali prioritari, funnel, ICP/segmenti, roadmap marketing.
- `campaigns.md` — campagne attive/passate. Ogni campagna: nome, periodo, canale, obiettivo, dati principali, insight, prossime azioni.
- `content.md` — piano contenuti, idee, temi editoriali, calendario, angoli comunicativi.
- `monitoraggio/` — report di monitoraggio campagna datati (`monitoraggio_adv_YYYY-MM-DD.md`).

## `website/`

- `website_notes.md` — struttura del sito, pagine, osservazioni su copy/UX/SEO/conversione, note sulla repo.
- `backlog.md` — task concreti sul sito. Ogni task: titolo, priorità (Alta/Media/Bassa), area (Copy/SEO/UX/Conversione/Tecnico), descrizione, motivo, criterio di completamento, stato.
- `homepage_copy.md` — copy definitivo della homepage.

## `decisions/`

- `decisions_log.md` — decisioni già prese, con motivazione e data. Non cancellare decisioni storiche.
- `open_questions.md` — domande aperte, ipotesi da validare, bloccanti. Quando una domanda si chiude, registra la decisione in `decisions_log.md` e marca la voce come risolta (non eliminarla).

## `reviews/`

Review operative ricorrenti, una per file datato:
- `weekly_review_YYYY-MM-DD.md` — pulse settimanale (dati + azioni).
- `maintenance_review_YYYY-MM-DD.md` — manutenzione della knowledge base.
- `founder-brief/brief_YYYY-MM-DD.md` — brief giornaliero del founder (routine `founder-daily-brief`).

I file `*.TEMPLATE.md` sono gli stampi da copiare.

## `missions/`

Missioni ambiziose gestite col **Relentless Outcome Workflow** (`workflows/relentless_outcome_workflow.md`): perseguono un *outcome*, non un task. Una sottocartella per missione; `_TEMPLATE/` è lo stampo.

## `products/`

Un workstream per ogni **prodotto proprio** con vita propria (roadmap, validazione, GTM), separato dalla memory marketing. `_TEMPLATE/` è lo stampo. Il codice dei prodotti vive nei rispettivi repo, non qui.

## `linkedin/`

Il **LinkedIn Growth OS**: distribuire il know-how in autorevolezza, conversazioni di qualità e opportunità commerciali. Profilo personale come motore. Vedi `linkedin/README.md`.

## `scheduled-tasks/`

Template dei task ricorrenti — "routine" (pulse, review, manutenzione, trend hunter, engagement radar, review missioni, brief founder…) + guida per ricrearli in Cowork. Vedi `scheduled-tasks/README.md`.

## `skills/`

Catalogo delle skill che si abbinano al kit (es. l'editor LinkedIn) + spazio per le tue (una sottocartella con `SKILL.md`). Vedi `skills/README.md`.

## `_inbox/`

Zona di scarico per materiale non ordinato. Butta qui file/note/export e di' *"processa l'inbox"*: Claude estrae i fatti e li archivia nei moduli giusti, in modo non distruttivo. Vedi `_inbox/README.md`.

## `examples/`

Un workspace reale, completo e **sanitizzato** (`examples/yempik/`): è lo *showcase* e il riferimento *few-shot* che l'installer usa come asticella di qualità. Non è il kit da compilare (quello è la root) — è la "soluzione".

---

## Convenzioni generali

- **Naming cartelle**: kebab-case.
- **File datati**: `nome_YYYY-MM-DD.md`.
- **Niente dati privati** nei file versionati pubblicamente: usa `{{placeholder}}` e tieni i contenuti reali fuori dal repo (vedi `.gitignore`).
- **Separare sempre** fatti, ipotesi e raccomandazioni.
