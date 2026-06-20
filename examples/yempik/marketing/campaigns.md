> **EN —** Filled example (sanitized): Yempik's Google Ads execution. Method/structure kept; budgets, tag IDs, client/competitor names → `[illustrativo]` / removed.
> **IT —** Esempio compilato (sanitizzato): esecuzione campagna Google Ads di Yempik. Metodo/struttura mantenuti; budget, ID tag, nomi clienti/competitor → `[illustrativo]` / rimossi.

---

# Yempik — Campagna Google Ads (esecuzione)

> Come la campagna è strutturata e gestita. Il *perché* dei cluster sta in `strategy.md`; i testi degli annunci in `content.md`.

> ⏸️ **STATO: CAMPAGNE FERMATE.** La campagna Google Ads è stata **messa in pausa** (ottimizzazione/budget). Implicazioni: (1) **la spesa paid si è interrotta**; (2) i task ROI **indipendenti dal paid** (money page automazione/software, case study, canali partner/formazione) diventano la priorità assoluta; (3) da chiarire se la pausa è **temporanea** o un **cambio di strategia** verso i canali non-paid. La struttura sotto descrive la campagna come configurata fino alla pausa.

## Impostazioni base
- **Tipo:** una sola campagna Search, obiettivo "Lead". Niente Performance Max, niente campagne intelligenti/AI (decisione di lancio).
- **Budget:** `[illustrativo]`/giorno, tutto sulla campagna commerciale.
- **Località:** Italia, opzione **"Presenza"** (non "presenza o interesse", per evitare clic dall'estero).
- **Lingua:** italiano.
- **Reti:** Display e Partner di ricerca **DISATTIVATI** (default attivi: su B2B bruciano budget).

## Struttura: 1 campagna «Commerciale / Lead», 4 gruppi di annunci
Ogni gruppo ha la sua lista di keyword stretta; tutti puntano alla landing. Match: `[esatta]` per alto intento/valore, `"frase"` per termini ampi ad alto volume. Broad match: **evitato** all'avvio.

**Gruppo 1 — Software house / su misura**
- `"software house"` · `[sviluppo software su misura]` · `[software gestionale personalizzato]` · `"gestionale su misura"` · `"software su misura"` · `"sviluppo software aziendale"` · `[consulenza digitalizzazione]`

**Gruppo 2 — Servizi AI B2B**
- `"consulenza intelligenza artificiale"` · `[intelligenza artificiale per aziende]` · `[ai per aziende]` · `"agenzia ai"` · `"agenzia intelligenza artificiale"` · `"sviluppo intelligenza artificiale"` · `"soluzioni di intelligenza artificiale"`

**Gruppo 3 — Agenti AI (volume)**
- `"ai agent"` · `"agente ai"` · `"agenti ai"` · `[creare un agente ai]` · `"assistente virtuale ai"`

**Gruppo 4 — Automazione processi**
- `"automazione processi aziendali"` · `"automazione aziendale"` · `"ottimizzare processi aziendali"` · `"digitalizzare azienda"` · `"automazione marketing"`

## Strategia di offerta (bidding) — roadmap
Account nuovo = zero dati: niente strategie automatiche all'inizio.

| Fase | Quando | Strategia |
|---|---|---|
| Avvio | Sett. 1–3 (0 conversioni) | CPC manuale (o "Massimizza clic" con tetto CPC) |
| Crescita | Da ~15–20 conv./mese | Massimizza conversioni |
| Maturità | 30+ conv./mese | CPA target |

**Problema CPC alti + budget piccolo:** alcune keyword costano molto. Con un budget contenuto un singolo clic costoso si mangia metà budget. **Soluzione:** tetti CPC sotto i picchi, accettando posizione media. Tetti CPC iniziali consigliati per gruppo: `[illustrativo]`.

## Negative keyword (lista a livello account)
`gratis · gratuito · free · corso · corsi · tutorial · significato · cos'è · come funziona · esempi · python · github · open source · download · pdf · wikipedia · login · accesso · studenti · tesi · università · stage · lavoro · stipendio · offerte lavoro · chatgpt gratis · giochi`

> **Le keyword navigazionali ad altissimo volume** (es. portali della PA) sono cruciali da escludere. Rivedere il rapporto "Termini di ricerca" ogni 2–3 giorni e ampliare le negative.

## Conversioni
- **Primaria (per l'offerta):** invio del form di contatto.
- **Secondarie:** clic su {{CHANNEL}} (canale chat), clic/chiamata sul telefono.
- Consent Mode v2 + banner cookie (CMP certificata) **obbligatori** in UE; 4 segnali (ad_storage, analytics_storage, ad_user_data, ad_personalization), default "denied".
- Attivare Enhanced Conversions for Leads (email hashed) per recuperare dati persi col consenso negato.
- Più avanti: tracciamento conversioni offline (quali lead diventano clienti) — la mossa a più alto impatto sulla pipeline.

> Stato tracciamento: **confermato funzionante** (tag + thank-you page `/start/grazie` + notifica email su ogni lead). Prime conversioni `[illustrativo]`, tutte dai gruppi **commerciali** (Software house, Servizi AI B2B), **0** da "Agenti AI (volume)" → conferma che converte l'intento commerciale, non il traffico DIY. Dettaglio in `reviews/`.

## KPI di riferimento
CTR > 3–5% · Tasso conv. clic→lead 3–6% · CPL `[illustrativo]` · Quality Score ≥ 7 · monitorare quota impressioni persa per budget. Metrica che conta davvero per l'obiettivo del fondatore: **quanti lead diventano progetti** (anche 1–2 buoni/mese ripagano).

## Ottimizzazione settimanale
- Sett. 1–2: raccolta dati, aggiungi negative, non toccare le offerte di continuo.
- Sett. 3–4: pausa alle keyword che spendono senza lead, alza i tetti CPC sui gruppi che portano contatti, passa a "Massimizza conversioni" a ~15–20 conv./mese.
- Dopo 4–6 settimane: sposta i gruppi che convertono in campagne proprie per dargli più budget.

> ⚠️ **Conflitto strategia ↔ dati.** L'ipotesi iniziale "pesa sul filone agenti/automazione, tieni Software house secondario" è stata **contraddetta dai dati**: le uniche conversioni arrivano dai gruppi **commerciali** — **Software house** è il miglior performer e **Servizi AI B2B** converte, mentre **"Agenti AI (volume)"** assorbe una quota alta della spesa con **0 conversioni**. La direzione validata dai dati è l'**opposto** dell'ipotesi: dare *più* peso a Software house + Servizi AI B2B e *ridurre* "Agenti AI" volume. L'ipotesi competitiva resta una tesi di lungo periodo (nicchia differenziata), ma **non** guida l'allocazione di budget oggi. Allineare `context/positioning.md`.

## Da completare
- Confermare i tetti CPC effettivamente impostati e l'avvenuta installazione del tracciamento conversioni.
- Correggere l'eventuale issue "gruppi senza annunci" (≥1 gruppo a 0 impression).
- Verificare che il click {{CHANNEL}} sia conversione "Principale" (è il canale che ha chiuso il primo lead).

**Informazioni mancanti per migliorare:** quale strategia di offerta è stata effettivamente impostata al lancio; ripartizione reale del budget tra i 4 gruppi.

> **Nota di metodo (ricorrente):** un'ipotesi di allocazione può essere **contraddetta dai dati** una volta arrivate le prime conversioni. Lascia l'ipotesi competitiva come tesi di lungo periodo, ma fa' guidare l'allocazione di budget dai dati.
