> **EN —** Filled example (sanitized): Yempik's marketing strategy. Method kept; all search volumes, CPCs, budgets, lead names → `[illustrativo]` / generalized.
> **IT —** Esempio compilato (sanitizzato): strategia di marketing di Yempik. Metodo mantenuto; volumi, CPC, budget e nomi lead → `[illustrativo]` / generalizzati.

---

# Yempik — Strategia di Marketing & Analisi della Domanda

> Il *perché* della strategia. L'esecuzione della campagna sta in `campaigns.md`; i testi degli annunci in `content.md`.

Fonte dati: Google Ads Keyword Planner via Supermetrics · Italia, italiano · valori in € (EUR). Dataset completo nel foglio di analisi keyword.

## Verdetto
**Sì, c'è spazio per fare advertising — ma non sul generico.** I termini generici ("intelligenza artificiale", "ai") fanno volumi enormi (`[illustrativo]`) ma con intento informativo (cercano ChatGPT, definizioni, news) e CPC bassissimo (`[illustrativo]`): brucerebbero budget senza lead.

## Mappa dei cluster (dal più al meno strategico per la lead gen)
> Volumi e CPC reali sostituiti con `[illustrativo]`.

| Cluster | Ricerche/mese | CPC medio | Intento |
|---|---|---|---|
| Agenti AI / Assistenti | `[illustrativo]` | `[illustrativo]` | Commerciale B2B — in crescita |
| Automazione | `[illustrativo]` | `[illustrativo]` | Commerciale B2B — bassa concorrenza |
| Servizi B2B / Consulenza | `[illustrativo]` | `[illustrativo]` | Commerciale B2B — alto valore |
| Sviluppo / Software | `[illustrativo]` | `[illustrativo]` | Commerciale B2B — alto valore |
| Formazione / Corsi | `[illustrativo]` | `[illustrativo]` | Commerciale B2C — volume |
| Generico / Awareness | `[illustrativo]` | `[illustrativo]` | Informativo — solo brand |

## La "gold mine"
1. **Agenti AI / Assistenti** — volume alto, tema in esplosione, concorrenza media: è esattamente ciò che Yempik sviluppa. Il filone con volume per spendere bene il budget.
2. **Automazione processi** — concorrenza BASSA, intento B2B chiaro, CPC contenuti. Filone sottovalutato.
3. **Servizi/Sviluppo B2B** — volumi piccoli MA CPC altissimi: i competitor pagano caro = mercato monetizzabile reale. Pochi clic, ognuno un potenziale progetto da migliaia di €. Keyword "soldi".
4. **Formazione/Corsi AI** — volume alto con intento d'acquisto: ottimo funnel B2C/prosumer **se** si offre formazione. Opportunità identificata, **non perseguita** al lancio.

## Sfumatura importante (allineamento col fondatore)
Le keyword "ai agent / agenti ai" sono ad alto volume **ma anche le più generiche**: vanno trattate come **layer di volume da qualificare** (con prezzo in landing e negative), non come lead già caldi. I lead "pronti all'acquisto" in Search sono di nicchia (poche centinaia di ricerche sui termini caldi): Google Search da solo porta **pochi lead ma di altissimo valore**.

## Trappole da evitare
- **Keyword navigazionale ad altissimo volume** (es. portali della PA): nessun intento commerciale → messa tra le negative.
- **Generico "ai" / "intelligenza artificiale"**: informativo, da non comprare.

## Lezione di metodo (sanitizzata, n=1)
Un primo lead serio è arrivato dal cluster **Automazione** via **click {{CHANNEL}}** (canale chat), mentre nel report Ads le *conversioni-evento* erano accreditate ad altri gruppi (commerciali). → **Conversione-evento ≠ cliente chiuso.** Non deprioritizzare un canale solo perché il report di piattaforma attribuisce la conversione altrove; segui il **ricavo reale**. Resta n=1: leggere come indizio forte, non come legge.

> ⚠️ **Correzione successiva:** il deal **non era ancora chiuso** (contratto non firmato, prezzo rinegoziato). La formulazione iniziale "primo cliente chiuso / soglia raggiunta / ROI positivo" era **prematura**: l'importo non è incassato finché non si firma. Stato reale: **preventivo/contratto inviato, in attesa di firma**. Il segnale di canale resta valido; il ricavo no. Vedi `decisions/decisions_log.md`.

## Economia della campagna (modello budget → lead)
Simulatore nel foglio di analisi keyword. **Tutti i tassi sono ipotesi da calibrare sui dati reali dopo le prime settimane.**

Scenario "Base" (ipotesi): budget `[illustrativo]`/mese · CPC `[illustrativo]` · conv. landing `[illustrativo]` · lead→SQL `[illustrativo]` · chiusura `[illustrativo]` · valore medio cliente **ipotizzato `[illustrativo]`** → `[illustrativo]` clic, `[illustrativo]` lead, `[illustrativo]` nuovi clienti/mese, CPL `[illustrativo]`, CPA `[illustrativo]`, ROAS `[illustrativo]`.

> Il valore medio cliente e i tassi di conversione/chiusura sono **assunzioni**, non dati storici. Vedi `decisions/open_questions.md`.

## Direzione strategica oltre la Search
Per fare **volume** la Search da sola non basta (domanda calda di nicchia): andrebbe abbinata la **demand generation** (LinkedIn/Meta) che *crea* domanda. Ipotesi non ancora decisa.

## Come si scala (metodo)
Bidding attuale = **"Massimizza conversioni"**: niente offerte manuali da alzare → su questa strategia il **budget** è la leva. Metodo di scaling, in ordine:
1. **Tracciamento lead→cliente — versione MANUALE adatta ai volumi attuali.** Il tracciamento offline *tecnico* (caricare i lead chiusi in Google per addestrare Smart Bidding) **non ripaga ora**: serve un volume di decine di conversioni/mese, mentre Yempik chiude poche vendite/mese → troppo poche perché l'algoritmo impari. Alla scala attuale basta una **tabella (Airtable): lead → keyword/canale → chiuso sì/no → valore**, e la decisione la prende l'umano. Il tracciamento offline tecnico diventa utile solo con ~20-30 lead/mese stabili. Verificare comunque che il **click {{CHANNEL}}** sia conversione **"Principale"** (è il canale che ha chiuso il primo lead).
2. **Tetto di CAC** ancorato al margine: con margine alto, anche un CAC relativamente alto resta multiplo dell'investimento. Finché cliente acquisito < tetto, si continua a versare.
3. **Loop:** budget +20-30% per volta (non triplicarlo: rientra in apprendimento) → attesa 1-2 settimane → CAC ancora sotto il tetto? Sì → rialza; No → ferma/ottimizza. Ripeti.
4. **Quando Search satura** (poche conversioni profittevoli in più, impression share alta): prima più keyword/varianti adiacenti; poi **un secondo motore di ricerca low-cost** (B2B); solo alla fine LinkedIn/Meta (creano domanda, payback lungo).
5. **Leve che battono i competitor:** conversione del sito (case study con numeri = leva n.1 per brand poco noto) + margine alto = vantaggio d'asta strutturale.

**Limite onesto:** tetto di domanda IT sui termini caldi (poche centinaia di ricerche/mese) → la Search può saturare a volume basso; oltre, la crescita richiede nuovi canali/domanda creata. n=1 cliente ≠ tasso medio.

## Da completare
- Decidere se attivare il funnel B2C "Formazione/Corsi" (anche solo come lead magnet).
- Decidere se aggiungere demand generation su LinkedIn/Meta.

**Informazioni mancanti per migliorare:** dati di conversione reali post-lancio per sostituire le ipotesi del simulatore; valore medio reale di un cliente acquisito.

## Opportunità: Formazione AI B2B come wedge commerciale
La formazione **C-level/responsabili di funzione** è un gioco a margine più alto del corso a catalogo: non lead-magnet, ma **porta d'ingresso ai progetti** (MVP 3.500 € / produzione 8.000 €). La formazione vende l'implementazione. Differenziatore già nostro — *"parli con chi costruisce"* — applicato alla formazione: non un docente generico, ma chi poi costruisce gli agenti. Possibili leve: gancio normativo come **contesto** (non come pitch) e **fondi interprofessionali** (tolgono l'obiezione prezzo). Raccomandazione: scala a livelli, prezzo a pacchetto non a ore, sezione "Formazione AI" sul sito collegata al funnel progetti. Decisioni in `decisions/open_questions.md`.

## Canale partner: agenzie come imbuto
Tesi: in search non c'è un fiume di domanda AI da catturare; la domanda è già **aggregata nei portafogli clienti** delle agenzie/web studio/software house generaliste, che ricevono richieste AI dai loro clienti PMI e non sanno evaderle. Yempik (forte nella delivery, debole nella domanda diretta) diventa il loro braccio tecnico.
- **Modello primario = white-label** (il partner tiene il cliente; Yempik invisibile), referral/co-brand come secondario.
- **Selezione per flusso clienti, non per fatturato.** Pochi partner buoni e ricorsivi.
- **Stato:** shortlist di agenzie verificate, bozza accordo, email outreach e brief pagina `/partner` pronti in `business-development/`.
- **Perché conta commercialmente:** sblocca progetti ricorrenti senza caccia al cliente finale uno alla volta, ed è complementare (non alternativo) alla Search e alla formazione (entrambe door-opener verso gli stessi progetti MVP/produzione).
