# Products

**A product workstream for every product you own — its own memory, separate from marketing.**
*Un workstream di prodotto per ogni prodotto che possiedi — memoria propria, separata dal marketing.*

---

## EN — The product-workstream pattern

When a company **owns a product** (not just sells services), that product develops a life of its own: a roadmap, design decisions, validation interviews, a go-to-market motion, early-access partners. Stuffing all of that into the general marketing memory makes both messy. So each owned product gets its **own folder** under `products/`.

A product workstream is the **product/GTM memory** — positioning, decisions, validation, the design-partner pipeline. It is **not** the codebase: the code and assets live in the product's own repository. This folder is where the *thinking* lives.

```
products/
├── _TEMPLATE/            # copy this for a new product
│   ├── README.md         # operational view: what it is / does / doesn't, stack, roadmap, pricing
│   ├── design-partners.md# early-access pipeline tracker
│   ├── validation.md     # validation-interview notes
│   └── decisions/
│       ├── decisions_log.md   # product-local decisions
│       └── open_questions.md  # product-local open questions & risks
└── {{PRODUCT}}/          # one folder per owned product
```

### Three rules that keep it clean

1. **Product memory ≠ marketing memory.** A product's decisions, validation and roadmap live here, under `products/{{PRODUCT}}/`. Company-wide decisions (that happen to touch the product) go in the OS-wide `decisions/decisions_log.md`. When in doubt, pick the most specific file and don't duplicate.
2. **Code lives in its own repo.** This folder holds no source code. It points *to* the repo as the **primary source of facts** ("the live page says X"), and clearly marks anything not grounded there as *assumption* or *to verify*.
3. **Don't invent.** If validation interviews haven't happened, `validation.md` stays an empty template. If no design partners are signed, the pipeline table stays blank. Missing data is listed honestly under "what's missing", never filled with plausible fiction.

### How to start a product workstream

1. **Copy `_TEMPLATE/`** to `products/{{PRODUCT}}/` (kebab-case the folder name).
2. Fill `README.md` from the **product's repo / live page** first — that's the source of truth. Mark anything else as assumption.
3. Open `decisions/open_questions.md` and dump every unknown (pricing model, naming risk, integration status…).
4. As decisions get made, move them to `decisions/decisions_log.md` with a reason and a date.
5. Track early-access slots in `design-partners.md`; record interviews in `validation.md`.
6. Keep the product's positioning consistent with the company `context/positioning.md`.

> If the repo is shared publicly, keep real partner names, customer quotes, prices and metrics **out**. Use `{{PLACEHOLDERS}}` and keep sensitive content local.

---

## IT — Il pattern del workstream di prodotto

Quando un'azienda **possiede un prodotto** (non vende solo servizi), quel prodotto prende vita propria: roadmap, decisioni di design, interviste di validazione, un go-to-market, partner in early access. Ficcare tutto questo nella memoria marketing generale fa diventare disordinate entrambe. Per questo ogni prodotto proprio ha la sua **cartella** sotto `products/`.

Un workstream di prodotto è la **memoria di prodotto/GTM** — posizionamento, decisioni, validazione, pipeline dei design partner. **Non** è il codice: codice e asset vivono nel repo del prodotto. Questa cartella è dove vive il *ragionamento*.

```
products/
├── _TEMPLATE/            # copia questo per un prodotto nuovo
│   ├── README.md         # vista operativa: cos'è / cosa fa / cosa NON fa, stack, roadmap, pricing
│   ├── design-partners.md# tracker pipeline early access
│   ├── validation.md     # note interviste di validazione
│   └── decisions/
│       ├── decisions_log.md   # decisioni locali al prodotto
│       └── open_questions.md  # domande aperte e rischi locali
└── {{PRODUCT}}/          # una cartella per prodotto proprio
```

### Tre regole che la tengono pulita

1. **Memoria di prodotto ≠ memoria marketing.** Decisioni, validazione e roadmap del prodotto vivono qui, sotto `products/{{PRODUCT}}/`. Le decisioni di portata aziendale (che toccano anche il prodotto) vanno nel `decisions/decisions_log.md` globale dell'OS. Nel dubbio, scegli il file più specifico e non duplicare.
2. **Il codice vive nel suo repo.** Questa cartella non contiene codice sorgente. Punta *al* repo come **fonte primaria dei fatti** ("la pagina live dice X") e marca chiaramente come *ipotesi* o *da verificare* tutto ciò che non viene da lì.
3. **Non inventare.** Se le interviste di validazione non sono state fatte, `validation.md` resta un template vuoto. Se non ci sono design partner firmati, la tabella pipeline resta vuota. I dati mancanti vanno elencati onestamente sotto "informazioni mancanti", mai riempiti con finzione plausibile.

### Come avviare un workstream di prodotto

1. **Copia `_TEMPLATE/`** in `products/{{PRODUCT}}/` (nome cartella in kebab-case).
2. Compila `README.md` partendo dal **repo / pagina live del prodotto** — è la fonte di verità. Marca tutto il resto come ipotesi.
3. Apri `decisions/open_questions.md` e scarica ogni incognita (modello di prezzo, rischio naming, stato integrazioni…).
4. Man mano che le decisioni si prendono, spostale in `decisions/decisions_log.md` con motivazione e data.
5. Traccia i posti early access in `design-partners.md`; registra le interviste in `validation.md`.
6. Tieni il posizionamento del prodotto coerente con `context/positioning.md` dell'azienda.

> Se il repo è pubblico, tieni **fuori** nomi di partner reali, citazioni dei clienti, prezzi e metriche. Usa i `{{PLACEHOLDER}}` e mantieni i contenuti sensibili in locale.
