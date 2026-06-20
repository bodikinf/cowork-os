> **EN —** Filled example (sanitized): one of Yempik's weekly marketing pulses. Structure/method kept; account & team IDs, budgets, lead/partner names, CPA figures → `[illustrativo]` / removed.
> **IT —** Esempio compilato (sanitizzato): una weekly pulse di marketing di Yempik. Struttura/metodo mantenuti; ID account e team, budget, nomi lead/partner, CPA → `[illustrativo]` / rimossi.

---

# Yempik — Weekly Marketing Pulse

**Data:** 2026-06-16 (mar) · **Periodo target:** settimana precedente
**Fonti tentate:** Supermetrics → Google Ads · GA4 (`yempik.com`) · Keyword Planner · Google Trends · repo del sito · file di progetto
**Valuta:** EUR · **Esecuzione:** task schedulato (autonomo)

> Convenzione: `[DATO REALE]` = numeri verificati da fonte · `[IPOTESI]` = lettura non provata · `[RACCOMANDAZIONE]` = azione proposta (le modifiche all'account Ads le applica la persona responsabile).

---

> ⛔ **BLOCCO DATI — SECONDA SETTIMANA CONSECUTIVA. Leggere prima di tutto.** Tutte le query Supermetrics (Google Ads, GA4, Keyword Planner, Google Trends) restituiscono lo stesso errore: **il free trial del team è scaduto**. → Questa pulse, come la precedente, **non contiene numeri freschi**. L'ultimo snapshot dati reale resta la weekly di inizio mese. Niente dati inventati (regola di Project).
>
> ⚠️ **Precisazione tecnica utile.** Lo stato di connessione delle sorgenti risulta `AUTHENTICATED` (OAuth valido): **il problema non è la connessione, è l'abbonamento.** Il gate è il trial scaduto a livello di team, non un token da riautorizzare. → Riautenticare non sblocca nulla: serve un **piano Supermetrics** oppure un **feed manuale**.

---

## 1) Executive summary

`[DATO REALE]` **Sono ormai due settimane che il marketing di Yempik vola senza strumenti.** La pipeline dati è offline e la decisione su come sanarla — flaggata come rischio 🔴 la settimana scorsa — **non è stata presa**. Nel frattempo il budget è stato alzato *(`[illustrativo]`/giorno)*: significa giorni di spesa pubblicitaria senza alcun monitoraggio incrociato su quale gruppo/keyword stia rendendo.

`[IPOTESI]` Il danno è contenuto ma reale: le **conversioni Ads sono comunque confermate** (notifica email su ogni lead) e la **UI nativa di Google Ads/GA4 resta consultabile**, quindi il conteggio lead non è perso. Ciò che manca è la **lettura di efficienza** (CPA per gruppo, impression share persa, effetto del budget aumentato) che permette di spostare budget con cognizione. Ogni settimana cieca è budget allocato "a sentimento".

`[DATO REALE]` La buona notizia è che il lavoro a più alto ROI **non dipende dai dati** ed è fermo da settimane: le **due money page sui cluster che convertono** (`/automazione-processi-aziendali`, `/software-su-misura`) sono ancora **inesistenti**, benché siano in backlog ALTA. In parallelo si è aperto molto sul fronte commerciale **non-paid**: linea **Formazione AI B2B**, **canale partner** (alcune agenzie contattate su LinkedIn) e **enti accreditati** da agganciare per la formazione finanziata. Questi sono i motori di crescita più concreti della settimana.

**Priorità della settimana:** (1) chiudere la decisione dati — è il rischio che si trascina; (2) spedire la money page automazione (il lavoro ROI fermo da troppo); (3) muovere i canali commerciali caldi, che oggi valgono più di qualsiasi ottimizzazione d'asta.

---

## 2) Dati / segnali più importanti

| Segnale | Stato | Fonte |
|---|---|---|
| Pipeline dati Supermetrics | ⛔ **Offline** (trial scaduto) | Errore query |
| Decisione sblocco dati | 🔴 **Ancora non presa** | `open_questions.md` |
| Budget campagna | 🟠 **Alzato** *(`[illustrativo]`)* — giorni non misurati | `campaigns.md` |
| Issue "gruppi senza annunci" | 🔴 Aperta (≥1 gruppo a 0 impression) — stato non verificabile da qui | `campaigns.md` |
| Money page automazione + software | 🔴 **Ancora inesistenti** (ALTA) | `website/backlog.md` |
| Linea Formazione AI B2B | 🟢 In definizione; one-pager + programma esteso pronti | `marketing/content.md` |
| Canale partner | 🟢 **Attivato** — richieste LinkedIn inviate, in attesa | `business-development/` |
| Enti accreditati | 🟢 Identificati, **da contattare** | `business-development/` |
| Registro lead inbound | 🟠 Ancora assente | `open_questions.md` |

`[DATO REALE]` Tre fatti che contano: (1) il rischio dati **non è più solo "nuovo", è cronico** — due pulse di fila senza numeri mentre la spesa è alta; (2) il lavoro sito ad alto impatto è **indipendente dal blocco** e resta non fatto; (3) la settimana ha spostato il baricentro commerciale verso canali **non-paid** (formazione, partner, enti) che maturano a prescindere dai dati Ads.

---

## 3) Performance campagne

⛔ **Non disponibile** (Supermetrics offline). Nessun dato fresco su impression, click, spesa, conversioni, impression share o ripartizione per gruppo.

`[DATO REALE — ultimo noto, dalla weekly precedente]` Base da cui ripartire appena i dati tornano (numeri reali sostituiti con `[illustrativo]`):

| Gruppo | Click | Spesa | Conv. | CPA | Lettura |
|---|---:|---:|---:|---:|---|
| **Software house / su misura** | `[illustrativo]` | `[illustrativo]` | `[illustrativo]` | `[illustrativo]` | miglior performer |
| **Servizi AI B2B** | `[illustrativo]` | `[illustrativo]` | `[illustrativo]` | `[illustrativo]` | converte, CPA più alto |
| Agenti AI (volume) | `[illustrativo]` | `[illustrativo]` | 0 | — | quota alta di spesa, 0 conv. |
| Automazione processi | `[illustrativo]` | `[illustrativo]` | 0 | — | canale del primo lead (via canale chat) |

`[RACCOMANDAZIONE]` Appena la pipeline torna, **prima query** = questa tabella per il periodo cieco, per verificare: (a) effetto del budget aumentato, (b) se l'issue "gruppi senza annunci" ha distorto la distribuzione, (c) se la lettura "pesare sui commerciali, ridurre Agenti AI volume" regge su più dati. Finché è giù, l'allocazione di riferimento resta l'ultima nota.

---

## 4) Insight GA4

⛔ **Non disponibile** (stessa causa). Nessun dato fresco su sessioni, engagement, sorgenti o pagine.

`[DATO REALE — ultimo noto]` Traffico paid su `/start` con engagement intorno al `[illustrativo]`; `/start/grazie` raggiunto (funnel form completo); primo **traffico organico** sulle 8 guide SEO/GEO.

> Promemoria di Project: GA4 è in differita e le conversioni Ads sono confermate (email su ogni lead) → l'assenza di numeri GA4 qui è il **blocco Supermetrics**, non un problema di tracking. Nessun gap di tracking da flaggare.

---

## 5) Keyword / trend rilevanti

⛔ **Refresh non disponibile** (Keyword Planner e Google Trends passano dallo stesso team Supermetrics bloccato).

`[DATO REALE — riferimento stabile, da `marketing/strategy.md`]` La mappa keyword non cambia settimana per settimana. Cluster monetizzabili confermati: **Agenti AI/Assistenti** (volume), **Automazione** (concorrenza bassa), **Servizi/Sviluppo B2B** ("keyword soldi"), **Formazione/Corsi AI** (oggi rilevante perché la **linea formazione è stata aperta**). Il refresh trend serve a confermare la stagionalità, non è un blocco al lavoro corrente.

`[IPOTESI]` Con la linea Formazione AI ora attiva, il cluster "Formazione/Corsi AI" passa da "opportunità mappata e non perseguita" a **keyword da presidiare** (organico via pagina `/formazione-aziende` + eventuale gruppo Ads dedicato). Da quantificare appena i dati tornano.

---

## 6) Problemi / opportunità sul sito `[da website/backlog.md + website_notes.md, indipendente dal blocco dati]`

**Opportunità ad alto ROI (ALTA), eseguibili subito — ferme da settimane:**
- 🟢 **Money page `/automazione-processi-aziendali`** — *non esiste*. È il cluster che ha chiuso il primo lead, CPC bassi: una pagina organica cattura in gratis la domanda che oggi paghiamo in paid.
- 🟢 **Money page `/software-su-misura`** — *non esiste*. Software house = gruppo con CPA più basso, CPC di mercato alti: ROI strutturale.
- 🟢 **2° case study = Automazione** — oggi i 2 case study sono entrambi voce: la prova è dove NON converte.
- 🟢 **Pagina `/formazione-aziende`** — brief pronto. Packaging del corso; le 8 guide già live ne sono la prova. Sblocca la nuova linea formazione.
- 🟢 **Pagina `/partner`** — brief pronto. Serve a convertire l'outreach partner già partito.

**Rischi/coerenza da chiudere (live, indicizzati):**
- 🔴 **Testimonial** `quoteDraft: true` ma **renderizzato live** in homepage → rischio legale/di fiducia sul principale social proof.
- 🟡 Placeholder **"P.IVA: da confermare"** su una pagina prodotto indicizzata → sostituire con l'entità legale.
- 🟡 **Link interni** dalle guide organiche verso money page + `/start` + case study.
- 🟡 **Coerenza "Made in Italy" ↔ entità legale** per answer engine e attrito fatturazione.

> `[DECISIONE]` Confermata la regola "**niente finte dashboard**": dove serve un visivo, design/mockup veri, mai dati inventati. Nessuna rimozione necessaria nel codice (verificato: la card incriminata non è mai entrata in repo).

---

## 7) Decisioni / domande aperte rilevanti

**Più urgente (si trascina):**
- 🔴 **Sblocco dati Supermetrics:** trial scaduto, decisione **ancora non presa**. Opzioni: piano Supermetrics **oppure** feed manuale settimanale (~6 numeri Ads + 3 GA4 incollati a mano). Ogni settimana di rinvio = budget paid allocato al buio.

**Aperte e commercialmente calde:**
- 🟢 **Canale partner — termini economici da definire** (sconto white-label, fee referral): servono per la prima call con un partner che accetta.
- 🟢 **Enti accreditati:** sequenza confermata (prima clienti, poi catalogo); **da contattare**.
- 🟡 **Formazione:** modello di prezzo a pacchetto (non €/h), edizione pilota dalla rete a prezzo amico per costruire prova/testimonial.
- 🟠 **Registro lead inbound:** ancora assente con più lead vivi + pipeline partner.
- 🟠 **Account Google Ads** (nuovo vs riuso), **connettore email "precondition failed"**: ancora aperte.

---

## 8) Priorità marketing della settimana

1. **Chiudere la decisione dati** — piano Supermetrics o feed manuale. È il rischio cronico: due pulse cieche di fila, budget alto. Moltiplicatore di tutto il resto.
2. **Spedire la money page `/automazione-processi-aziendali`** — il lavoro a ROI più alto e zero dipendenza dai dati, fermo da settimane. Cattura in organico la domanda che paghiamo in paid sul cluster che chiude.
3. **Muovere i canali commerciali caldi** — contattare gli enti accreditati (già clienti → formazione finanziata, la via più rapida a fatturato) e presidiare le accettazioni partner su LinkedIn con i termini economici pronti.

---

## 9) 5 azioni consigliate `[RACCOMANDAZIONE]` (ordinate per impatto commerciale)

1. **Sbloccare i dati questa settimana.** Decisione binaria: piano Supermetrics **o** feed manuale (bastano impression, click, spesa, conv. + CPA dei 2 gruppi commerciali da Google Ads; sessioni paid, engagement, view `/start/grazie` da GA4). Senza, la prossima pulse è la terza cieca.
2. **Contattare gli enti accreditati.** Sono **già clienti, già accreditati**: è la porta più veloce a fatturato (loro come clienti del corso = land + trial; poi catalogo per i loro clienti). Inquadrare la finestra "budget formazione da usare entro fine anno" value-first.
3. **Spedire la money page `/automazione-processi-aziendali`**: H1 transazionale, 3 flussi concreti, prezzi, `serviceSchema`+FAQ, link a `/prezzi` e case study. Domanda che oggi paghiamo, catturata gratis.
4. **Presidiare il canale partner:** monitorare le accettazioni degli inviti LinkedIn, preparare il DM di follow-up, e **fissare i termini economici** (sconto white-label / fee referral) così la prima call può chiudere invece di rimandare.
5. **Chiudere i due rischi di fiducia sul sito live:** confermare/gate del testimonial e rimuovere il placeholder "P.IVA: da confermare". Entrambi indicizzati, entrambi a costo-zero di fix.

---

## 10) File aggiornati / da aggiornare

**Aggiornati in questo run:** creato questo file; `decisions/open_questions.md` (rischio dati non risolto + precisazione OAuth-vs-abbonamento); `marketing/campaigns.md` (nota: blocco confermato, OAuth attivo ma trial scaduto).
**Da aggiornare (azione esterna):** decisione abbonamento/feed dati; registro lead inbound; conferma chiusura issue "gruppi senza annunci"; termini economici accordo partner.

---

## Memory Update

- **File aggiornati:** `reviews/weekly_review_2026-06-16.md` (creato); `decisions/open_questions.md` (rischio dati aggiornato); `marketing/campaigns.md` (nota blocco confermato).
- **Decisioni aggiunte:** nessuna nuova confermata (lo sblocco dati resta domanda aperta).
- **Domande aperte aggiunte:** nessuna nuova; **escalation** di quella esistente (sblocco dati: da "nuovo rischio" a "rischio cronico, 2ª settimana").
- **Ipotesi aggiunte:** lo stato `AUTHENTICATED` delle sorgenti è OAuth valido — il blocco è l'abbonamento/trial di team, non il token (riautenticare non sblocca).
- **Task aggiunti:** decidere sblocco dati; spedire money page automazione; contattare enti accreditati; presidiare accettazioni partner + fissare termini economici; chiudere rischi sito (testimonial, P.IVA pagina prodotto).
- **Rischi aggiunti:** 🔴 **blocco dati cronico** (2 pulse cieche consecutive) con budget alto → spesa non valutabile; rischio raffreddamento pipeline (lead inbound + partner) senza registro e senza follow-up.
- **Opportunità aggiunte:** enti accreditati già clienti = via rapida a fatturato formazione; canale partner attivo = pipeline ricorrente; money page automazione/software = ROI alto indipendente dai dati.
- **Prossime azioni:** (1) sbloccare i dati (piano o feed); (2) parte la money page automazione; (3) outreach enti accreditati; (4) prossima pulse — se i dati tornano, primo refresh = performance per gruppo + effetto budget aumentato.
