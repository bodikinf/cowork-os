# {{PRODUCT}} — {{PRODUCT_ONE_LINER}}

> **EN —** The operational view of an owned product: what it is, what it does and doesn't, the stack, roadmap, pricing and the design-partner program. The product's repo/live page is the source of truth; mark anything not grounded there as *assumption* or *to verify*. This is product/GTM memory, not code.
> **IT —** La vista operativa di un prodotto proprio: cos'è, cosa fa e cosa non fa, lo stack, la roadmap, il pricing e il programma design partner. Il repo/pagina live del prodotto è la fonte di verità; marca come *ipotesi* o *da verificare* tutto ciò che non viene da lì. Questa è memoria di prodotto/GTM, non codice.

> Workstream di prodotto proprio di {{COMPANY}}.
> **Fonte primaria dei fatti:** repo `{{PRODUCT_REPO}}` (pagina live `{{LIVE_PAGE}}`, componenti `{{COMPONENTS_PATH}}`). Quanto qui non viene da lì è marcato come *ipotesi* o *da verificare*.

---

## In una riga
{{PRODUCT}} è {{WHAT_IT_IS}} che {{WHAT_IT_DOES}}. Posizionamento: *"{{POSITIONING_TAGLINE}}"*.

- **Mercato:** {{TARGET_MARKET}}.
- **Da:** {{COMPANY}} ({{WHY_THIS_PRODUCT}} — es. prodotto-lab + prova di competenza su {{CAPABILITY}}).
- **Stato:** {{PRODUCT_STATUS}} *(es. in sviluppo attivo / programma design partner aperto).*
- **Pagina live:** `{{LIVE_PAGE}}`.

## Cosa fa (i passi)
{{HOW_IT_WORKS_STEPS}}

1. **{{STEP_1_NAME}}** — {{STEP_1_DESC}}.
2. **{{STEP_2_NAME}}** — {{STEP_2_DESC}}.
3. **{{STEP_3_NAME}}** — {{STEP_3_DESC}}.
4. **{{STEP_4_NAME}}** — {{STEP_4_DESC}}.

## {{SECONDARY_SURFACE}} *(es. la dashboard, l'app, il pannello)*
{{SECONDARY_SURFACE_DESC}} — *l'altra faccia del prodotto oltre alla funzione principale.*

- **{{AREA_1}}** — {{AREA_1_DESC}}.
- **{{AREA_2}}** — {{AREA_2_DESC}}.
- **{{AREA_3}}** — {{AREA_3_DESC}}.

## Cosa NON fa (confini, per scelta)
I confini sono una **decisione di prodotto**, non una mancanza. Definiscono fiducia e gestione del rischio.

- **Non {{BOUNDARY_1}}** → {{BOUNDARY_1_INSTEAD}}.
- **Non {{BOUNDARY_2}}** → {{BOUNDARY_2_INSTEAD}}.
- **Non {{BOUNDARY_3}}** → {{BOUNDARY_3_INSTEAD}}.
- Regola unica: *{{SINGLE_RULE}}* *(es. se tocca soldi, atti legali o emergenze, decide chi è pagato per decidere).*

## Sicurezza e conformità
{{SECURITY_NOTES}} *(es. conforme GDPR; ruoli e permessi; storico verificabile; dati ospitati in UE; DPA prima dell'onboarding).*

---

## Stack tecnico
{{TECH_STACK}} *(usa nomi di tool generici, es. provider telefonia, provider voce, framework frontend, DB; nessun account ID o link privato).*
> Codice e asset vivono nel repo `{{PRODUCT_REPO}}`, non qui.

## Integrazioni previste
{{INTEGRATIONS}} — *con cosa si affianca/si integra e in quale fase.* Marca come *previste* finché non sono in produzione.

## Roadmap
| Fase | Periodo | Contenuto |
|---|---|---|
| 1 — {{PHASE_1}} | **{{PHASE_1_PERIOD}}** | {{PHASE_1_CONTENT}} |
| 2 — {{PHASE_2}} | **{{PHASE_2_PERIOD}}** | {{PHASE_2_CONTENT}} |
| 3 — {{PHASE_3}} | **{{PHASE_3_PERIOD}}** | {{PHASE_3_CONTENT}} |

## Pricing
- **Listino (a regime):** {{LIST_PRICE}}.
- **Programma early access:** {{EARLY_ACCESS_PRICE}}, poi {{POST_EARLY_ACCESS_TERMS}}.

> ⚠️ *Da verificare:* {{PRICING_TO_VERIFY}} *(prezzo ufficiale a regime, unità di misura, eventuali tier).* Tieni i prezzi reali fuori da un repo condiviso se sensibili.

## Programma design partner
{{N_SLOTS}} posti, {{SELECTION_CRITERIA}}. *"{{DESIGN_PARTNER_PROMISE}}"* *(es. "Vogliamo costruire il prodotto con voi, non per voi").*

**Cosa ottiene il partner:** {{PARTNER_GETS}} *(es. accesso anticipato + onboarding completo; prezzo early access; setup white-glove; linea diretta col team; influenza sulle priorità di sviluppo).*

**Cosa dà il partner:** {{PARTNER_GIVES}} *(es. call di feedback settimanale; case study scritto dopo {{DAYS}} giorni; reference call/mese; permesso di citarlo — logo, testimonial).*

**Form di candidatura** (`{{FORM_PATH}}`): {{FORM_FIELDS}} → {{FORM_ENDPOINT}}. Risponde {{FOUNDER}} entro {{SLA}}. Pipeline tracciata in `design-partners.md`.

---

## Marketing & sito
- **Aggancio campagna:** {{CAMPAIGN_HOOK}} *(quale ad group / keyword / pagina porta traffico al prodotto).*
- **Brand asset:** {{BRAND_ASSETS_PATH}} *(dove vivono logo e varianti, nel repo del prodotto).*
- **Issue tecniche aperte sul sito:** {{OPEN_SITE_ISSUES}} — dettaglio in `decisions/open_questions.md`.

## ⚠️ Rischio naming (se applicabile)
{{NAMING_RISK}} *(es. esiste un concorrente con nome simile → valutare impatto su SEO/marchio).* Tracciato in `decisions/open_questions.md`.

---

## Struttura cartella
- `README.md` — questo file (vista operativa).
- `decisions/decisions_log.md` — decisioni locali al prodotto.
- `decisions/open_questions.md` — domande aperte e rischi locali.
- `design-partners.md` — tracker pipeline dei posti early access.
- `validation.md` — note interviste di validazione.

> Il **codice e gli asset** del prodotto vivono nel repo `{{PRODUCT_REPO}}` (non qui). Questa cartella è la **memoria di prodotto/GTM**.

## Informazioni mancanti (da non inventare)
Elenca onestamente ciò che ancora non sai. Non riempirlo con finzione plausibile.
- {{MISSING_1}} *(es. dati reali delle interviste di validazione — oggi `validation.md` è vuoto).*
- {{MISSING_2}} *(es. design partner effettivamente firmati / in pipeline).*
- {{MISSING_3}} *(es. metriche/KPI reali del prodotto).*
- {{MISSING_4}} *(es. conferma del listino e del modello di prezzo a regime).*

---

> Un workstream di prodotto compilato e sanitizzato (Yempik — un agente vocale verticale) vive in `examples/yempik/products/voice-agent-verticale/README.md`. Regola di anonimizzazione: in un repo condiviso il nome reale del prodotto, i nomi dei design partner, i prezzi e le metriche reali restano **fuori** (prezzi `[illustrativo]`).
