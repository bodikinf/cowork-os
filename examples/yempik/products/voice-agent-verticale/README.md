# Voice agent verticale — *esempio compilato* (Yempik)

> **EN —** Filled, sanitized example of `products/_TEMPLATE/README.md` for a Yempik-owned voice-agent product. The real product brand and vertical, the design-partner names, the real stack vendors and the real prices are removed; prices are `[illustrativo]` and the vertical is described generically.
> **IT —** Esempio compilato e sanitizzato di `products/_TEMPLATE/README.md` per un prodotto voice-agent di Yempik. Il brand reale e il verticale reale del prodotto, i nomi dei design partner, i vendor reali dello stack e i prezzi reali sono rimossi; i prezzi sono `[illustrativo]` e il verticale è descritto in modo generico.

> Workstream di prodotto proprio di **Yempik**.
> **Fonte primaria dei fatti:** repo del prodotto (`yempik-website`, pagina live `/prodotti/<prodotto>`, componenti e asset relativi). Quanto qui non viene da lì è marcato come *ipotesi* o *da verificare*. Questa è memoria di prodotto/GTM, non codice.

---

## In una riga
È un **agente vocale conversazionale** verticale su una **nicchia di servizi con un dolore chiaro sul telefono** (molte chiamate ripetitive, uno studio/ufficio piccolo che non riesce a rispondere a tutti). Risponde al telefono, filtra le chiamate, apre pratiche, coordina i fornitori e restituisce tutto in una **dashboard ordinata**, con recap giornaliero. Posizionamento: *"Centralino in ordine — si affianca, non sostituisce il gestionale esistente."*

- **Mercato:** una nicchia verticale di micro/PMI di servizi in Italia (descritta in modo generico per anonimato).
- **Da:** Yempik (prodotto-lab + prova di competenza sugli agenti vocali).
- **Stato:** in sviluppo attivo / programma design partner aperto.
- **Pagina live:** `/prodotti/<prodotto>` (indicizzata, riceve già traffico organico).

## Cosa fa (i 4 passi)

1. **Riceve** — risponde al numero dello studio (invariato, nessun porting), al primo squillo, 24/7.
2. **Riconosce** — identifica il chiamante e il suo contesto (es. una pratica aperta da qualche giorno, un appuntamento imminente). Non risponde mai "a freddo".
3. **Agisce** — se è informativa risponde da sola; se è un'esigenza operativa contatta il fornitore di fiducia, fissa l'appuntamento, riconferma al chiamante.
4. **Riporta** — ogni sera un recap: chiamate gestite, pratiche schedulate, chi deve richiamare il titolare.

## La dashboard
Non è solo voce: è anche la regia dove "tutto quello che succede al telefono torna sulla scrivania".

- **Oggi** — feed del giorno in tempo reale + colonna "chi devi richiamare tu".
- **Pratiche** — kanban drag-and-drop; ogni pratica linka transcript, audio e decisione presa.
- **Fornitori** — pool a livello studio: contatti autorizzati, SLA medio di risposta, interventi recenti.
- **Conoscenza** — il sapere di ogni cliente/contesto (regole, recapiti, FAQ, calendario) con editor inline; l'agente lo legge prima di parlare.

## Cosa NON fa (confini, per scelta)
I confini sono una **decisione di prodotto**, non una mancanza.

- **Non decide su soldi** (rateizzazioni, sconti, scadenze) → prende nota e gira la pratica.
- **Non firma atti legali** (verbali, lettere ufficiali) → restano firma del titolare.
- **Non è un risponditore IVR** ("digita 1…") → è conversazionale.
- **Non è un gestionale** → si affianca al gestionale di settore, non lo sostituisce.
- **Emergenze** → triage in pochi secondi, contatto reperibilità, alert in tempo reale; non le tratta da solo.
- Regola unica: *se tocca soldi, atti legali o emergenze, decide chi è pagato per decidere — il titolare.*

## Sicurezza e conformità
Conforme GDPR e pensato per dati sensibili di settore; ruoli e permessi per lo studio; transcript e storico sempre verificabili; **dati ospitati in UE**, **DPA prima dell'onboarding**. L'agente non prende decisioni vincolanti e non nasconde quello che fa.

---

## Stack tecnico
MVP in build su stack consolidato Yempik (nomi generici): **provider di telefonia** + **provider voce** + **AI SDK** + **database gestito**; frontend/landing in Next.js (repo `yempik-website`), hosting su PaaS. *(Nessun account ID o link privato.)*
> Codice e asset vivono nel repo del prodotto, non qui.

## Integrazioni previste
**Gestionali di settore** (contabilità/CRM verticale) — integrazione *prevista* nella fase design partner. L'agente si affianca, non sostituisce il gestionale. Marca come *prevista* finché non è in produzione.

## Roadmap
| Fase | Periodo | Contenuto |
|---|---|---|
| 1 — Validazione | **Oggi** | Interviste con operatori veri per raffinare il prodotto; MVP in build. |
| 2 — Pilota | **`[illustrativo]`** | Onboarding dei **primi design partner**; integrazione coi gestionali di settore; validazione del modello end-to-end. |
| 3 — Lancio | **`[illustrativo]`** | Lancio commerciale; primi studi attivi entro fine trimestre, poi scaling. |

## Pricing
- **Listino (a regime):** `[illustrativo]`/mese.
- **Programma design partner (early access):** `[illustrativo]`/mese flat per `[illustrativo]` mesi, indipendente dal volume chiamate. Dopo: si continua a listino oppure si esce senza penali.

> ⚠️ *Da verificare:* il listino a regime, l'unità di misura (per studio? per volume?) ed eventuali tier. I prezzi reali restano fuori da un repo condiviso.

## Programma design partner
`[illustrativo]` posti, selezione a rotazione, primi studi del verticale. *"Vogliamo costruire il prodotto con voi, non per voi."*

**Cosa ottiene il partner:** accesso anticipato con onboarding completo fatto da Yempik; prezzo early access `[illustrativo]`; setup white-glove; linea diretta col team; influenza diretta sulle priorità di sviluppo.

**Cosa dà il partner:** call di feedback settimanale (30 min); disponibilità a un case study scritto dopo ~60 giorni; una reference call/mese con prospect; permesso di citarlo pubblicamente (logo, testimonial).

**Form di candidatura** (`/prodotti/<prodotto>#form`): nome, email, nome studio, dimensione, telefono → endpoint email del sito. Risponde Raffaele entro 24h lavorative. Pipeline tracciata in `design-partners.md`.

---

## Marketing & sito
- **Aggancio campagna:** ad group "Voice / Centralino" della Search commerciale, keyword tipo `centralino virtuale` → sezione demo del prodotto.
- **Brand asset:** cartella brand nel repo del prodotto (mark, wordmark, lockup, varianti logo).
- **Issue tecniche aperte sul sito:** un placeholder "P.IVA da confermare" nel footer di una pagina indicizzata; uno schema `softwareApplication` con default sbagliato (tarato su un altro prodotto) da correggere per un voice agent. Dettaglio in `decisions/open_questions.md`.

## ⚠️ Rischio naming
Esiste un possibile concorrente con nome simile nel mercato → da valutare l'impatto su posizionamento, SEO e marchio. Tracciato in `decisions/open_questions.md`.

---

## Struttura cartella
- `README.md` — questo file (vista operativa).
- `decisions/decisions_log.md` — decisioni locali al prodotto.
- `decisions/open_questions.md` — domande aperte e rischi locali.
- `design-partners.md` — tracker pipeline dei posti early access.
- `validation.md` — note interviste di validazione.

> Il **codice e gli asset** del prodotto vivono nel repo del prodotto (non qui). Questa cartella è la **memoria di prodotto/GTM**.

## Informazioni mancanti (da non inventare)
- Dati reali delle interviste di validazione (n°, profili, insight) — `validation.md` è oggi un template vuoto.
- Design partner effettivamente firmati / in pipeline — `design-partners.md` è da popolare.
- Metriche/KPI reali del prodotto (oggi nessun numero misurato disponibile).
- Conferma del listino e del modello di prezzo a regime.

---

> *Sanitizzazione:* il nome reale del prodotto e del verticale, i vendor reali dello stack, i gestionali di settore citati per nome, i prezzi reali, il nome del concorrente e qualunque design partner sono stati **rimossi** o resi generici/`[illustrativo]`. La pipeline parte **vuota** (nessun partner reale). Restano Yempik, Raffaele, yempik.com.
