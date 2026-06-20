# Mission {{NN}} — {{MISSION_TITLE}}

> **EN —** The mission brief: the outcome, when it's done, the routes, and the rules of engagement. This is the first file you write and the one you re-read before every session. Update the *Mission status* line each time.
> **IT —** Il brief della missione: l'outcome, quando è fatta, le strade e le regole d'ingaggio. È il primo file che scrivi e quello che rileggi prima di ogni sessione. Aggiorna la riga *Stato missione* ogni volta.

> Gestita con il **Relentless Outcome Workflow** (`../../workflows/relentless_outcome_workflow.md`).
> Avviata {{DATE}} · {{OWNER_DIRECTIVE}} (es. "mission, carta bianca").

---

## Mission (outcome, non task)

{{MISSION_AS_OUTCOME}}

> Scrivi l'obiettivo come **risultato da ottenere**, non come attività da svolgere.
> ❌ Task: "Mandare una mail a {{TARGET}}."
> ✅ Outcome: "{{ONE_LINE_OUTCOME}}" (es. ottenere una conversazione concreta con {{TARGET}} su {{TOPIC}}).

Forme possibili dell'outcome (elenca le varianti accettabili, così l'esecuzione non si incastra su una sola idea):
{{POSSIBLE_FORMS}} *(es. call, risposta utile, percorso alternativo validato, proof of work pubblico abbastanza forte da riattivare la conversazione).*

## Definition of Done

La missione è completata quando almeno **una** di queste è vera:
- {{DOD_CONDITION_1}}
- {{DOD_CONDITION_2}}
- {{DOD_CONDITION_3}}
- {{DOD_CONDITION_4}}
- {{DOD_CONDITION_5}}

> Definisci anche **DoD intermedie controllabili** (milestone che dipendono da te, non dalla controparte): {{INTERMEDIATE_DOD}} *(es. N call di discovery fissate, pilota calendarizzato).*

## Posizionamento (vincolante)

Come ti presenti in questa missione — e cosa **non** dire mai.
- **NON** presentarti come {{ANTIPOSITIONING_1}}.
- **NON** presentarti come {{ANTIPOSITIONING_2}}.
- Presentati come: *{{POSITIONING_ONE_LINER}}*.
- Angolo unico (i chiodi, in quest'ordine): {{ANGLE_1}} · {{ANGLE_2}} · {{ANGLE_3}}.

> Tieni il posizionamento **coerente** con `context/positioning.md` dell'OS. Se la missione richiede un angolo nuovo, registralo come decisione in `decisions/decisions_log.md`.

## Tesi strategica

{{STRATEGIC_THESIS}}

> Una o due frasi: perché *tu* sei la persona/azienda giusta per questo outcome, e qual è il ponte tra ciò che offri e ciò di cui ha bisogno {{TARGET}}.

## Perché ORA (fatti verificati)

Elenca i **fatti datati e verificabili** che rendono questo il momento giusto. Solo fatti, con fonte; le ipotesi vanno marcate come tali.
- {{TIMING_FACT_1}} — fonte: {{SOURCE_1}}.
- {{TIMING_FACT_2}} — fonte: {{SOURCE_2}}.
- {{TIMING_FACT_3}} — fonte: {{SOURCE_3}}.

## Route Map (≥5 strade, mappate prima di agire)

Sintesi delle strade. Il dettaglio completo (ipotesi, asset, persone, rischio, probabilità, alternativa) sta in `route_map.md`.

1. {{ROUTE_1}}
2. {{ROUTE_2}}
3. {{ROUTE_3}}
4. {{ROUTE_4}}
5. {{ROUTE_5}}
6. {{ROUTE_6_OPTIONAL}}

> **Sequenza consigliata:** {{RECOMMENDED_SEQUENCE}} *(es. parti dalle route asincrone/in background, poi pubblica un proof of work, poi outreach diretto appoggiato al proof of work).*

## Route Execution Loop

Per **ogni** route attiva, gira questo ciclo (i campi vivono in `route_map.md`, gli esiti in `mission_log.md`):

`ipotesi → azione → asset necessari → persone/org → messaggio → rischio → probabilità (stima) → next step → risultato → alternativa se fallisce`

Regola madre: **se incontri un blocco, non concludere.** Riformula la missione → cerca un canale alternativo → riduci l'obiettivo → trova un proxy → costruisci proof of work → cerca una persona laterale → torna al risultato da un'altra strada.

## Funnel & numeri (ipotesi da calibrare — NON dati storici)

Se la missione è a volumi (vendite, lead, contatti), stima a ritroso. Marca tutto come **ipotesi**, non dato.
- Per chiudere **{{TARGET_NUMBER}}** servono ~{{N_CALLS}} {{STAGE_3}} → ~{{N_CONVOS}} {{STAGE_2}} → ~{{N_TOUCHES}} {{STAGE_1}} → ~{{N_ACCOUNTS}} account × {{CONTACTS_PER_ACCOUNT}} contatti.
- Tassi di conversione ipotizzati (da rivedere sui dati reali): {{ASSUMED_RATES}}.

## Evidence Log (sintesi)

Registro completo in `mission_log.md`. Tabella di riepilogo delle azioni chiave:

| Data | Route | Azione | Target | Stato | Risultato | Next |
|------|-------|--------|--------|-------|-----------|------|
| {{DATE}} | {{ROUTE}} | {{ACTION}} | {{TARGET}} | {{STATUS}} | {{RESULT}} | {{NEXT}} |

> Stati ammessi: `todo` · `in corso` · `done` · `partial` · `bloccato` · `WIN` · `scartata`.

## Escalation (cosa serve dalla persona)

L'agente prepara; la persona decide. Chiedi **solo** quando serve davvero: approvazioni di invio, scelte di posizionamento, accessi/login, budget.
- {{ESCALATION_ITEM_1}}
- {{ESCALATION_ITEM_2}}
- {{ESCALATION_ITEM_3}}

> Vincolo non negoziabile: **ogni comunicazione esterna va approvata prima dell'invio.** Niente spam, identità false, scraping aggressivo o messaggi automatici senza ok.

## Stop Condition

"Impossibile" si dichiara **solo** dopo aver fatto, e documentato, tutto questo:
- ≥5 route esplorate;
- {{N}} contatti/canali mappati (con {{CONTACTS_PER_ACCOUNT}} contatti per account dove ha senso);
- {{N}} messaggi preparati;
- {{N}} workaround tentati ({{WORKAROUND_EXAMPLES}});
- {{N}} proof of work prodotti;
- spiegazione esplicita del blocco;
- proposta della prossima opzione meno diretta.

> Finché esiste {{LAST_RESORT_CONDITION}} *(es. una funzione/persona raggiungibile che ha il problema che risolvi)*, la missione ha ancora una strada.

## Rischi (presidiati)

- {{RISK_1}} → mitigazione: {{MITIGATION_1}}.
- {{RISK_2}} → mitigazione: {{MITIGATION_2}}.
- {{RISK_3}} → mitigazione: {{MITIGATION_3}}.

## Stato missione

**{{CURRENT_PHASE}}.** Prodotti finora: {{ARTIFACTS_PRODUCED}}. Prossimo: {{NEXT_FOCUS}}.

---

> Una missione compilata e sanitizzata, dall'inizio alla fine (mission, route map, next actions, evidence log), vive in `examples/yempik/missions/partnership-vendor-ai/` (Yempik). Regola di anonimizzazione: in qualunque file condiviso il target va genericizzato e ogni nome di persona/azienda, contatto, data privata e numero reale resta **fuori**.
