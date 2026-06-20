> **EN —** The *why* of the marketing strategy: demand analysis, channels, funnel, scaling method. Update when the strategic reading changes. Campaign execution lives in `campaigns.md`.
> **IT —** Il *perché* della strategia di marketing: analisi della domanda, canali, funnel, metodo di scaling. Aggiornalo quando cambia la lettura strategica. L'esecuzione della campagna sta in `campaigns.md`.

---

# {{COMPANY}} — Strategia di Marketing & Analisi della Domanda

> Il *perché* della strategia. L'esecuzione della campagna sta in `campaigns.md`; i testi degli annunci in `content.md`.

Fonte dati: {{DATA_SOURCE — es. Keyword Planner via Supermetrics}} · {{MARKET}}, {{LANGUAGE}} · {{PERIOD}}.

## Verdetto
> Una riga di sintesi: c'è spazio per fare advertising? su cosa sì, su cosa no?
**{{VERDICT}}**

## Mappa dei cluster (dal più al meno strategico per la lead gen)
> Sostituisci i numeri con i tuoi dati reali; se il file è pubblico, tieni i volumi/CPC come `[illustrativo]`.

| Cluster | N. kw | Ricerche/mese | CPC medio | Intento |
|---|---|---|---|---|
| {{CLUSTER_1}} | `[illustrativo]` | `[illustrativo]` | `[illustrativo]` | {{intento}} |
| {{CLUSTER_2}} | `[illustrativo]` | `[illustrativo]` | `[illustrativo]` | {{intento}} |
| {{CLUSTER_3}} | `[illustrativo]` | `[illustrativo]` | `[illustrativo]` | {{intento}} |

## La "gold mine"
> I 2–4 cluster su cui concentrare il budget, con il motivo.
1. **{{GOLD_CLUSTER_1}}** — {{perché}}
2. **{{GOLD_CLUSTER_2}}** — {{perché}}

## Trappole da evitare
- **{{TRAP_KEYWORD}}** ({{volume}}): {{perché è traffico spazzatura / da mettere in negative}}.

## Economia della campagna (modello budget → lead)
> Un simulatore di scenari. **Tutti i tassi sono ipotesi da calibrare sui dati reali** dopo le prime settimane (vedi `decisions/open_questions.md`).
Scenario "Base" (ipotesi): budget `[illustrativo]`/mese · CPC `[illustrativo]` · conv. landing `[illustrativo]` · valore medio cliente **ipotizzato `[illustrativo]`** → `[illustrativo]` lead/mese, CPL `[illustrativo]`, CPA `[illustrativo]`.

## Come si scala (metodo)
> Il metodo è generico e riutilizzabile. Adattalo alla tua scala reale.
1. **Tracciamento lead→cliente.** A volumi bassi (poche vendite/mese) basta una **tabella (Airtable): lead → keyword/canale → chiuso sì/no → valore**, e la decisione la prende l'umano. Il tracciamento offline *tecnico* (caricare i lead chiusi per addestrare lo Smart Bidding) ripaga solo con ~20–30 conversioni/mese stabili.
2. **Tetto di CAC** ancorato al margine: finché il cliente acquisito costa meno del tetto, continui a versare.
3. **Loop:** budget +20–30% per volta (non triplicarlo: rientra in apprendimento) → attesa 1–2 settimane → CAC ancora sotto il tetto? Sì → rialza; No → ferma/ottimizza.
4. **Quando la Search satura:** prima più keyword/varianti adiacenti; poi un secondo motore di ricerca low-cost; solo alla fine i canali che *creano* domanda (payback lungo).
5. **Leve che battono i competitor:** conversione del sito (case study con numeri = leva n.1 per brand poco noto) + margine alto = vantaggio d'asta strutturale.

**Limite onesto:** il tetto di domanda sui termini caldi può essere basso → la Search satura a volume contenuto; oltre, serve nuova domanda/canali. n=1 cliente ≠ tasso medio.

## Da completare
- {{OPEN_ITEM_1 — es. attivare un funnel secondario? aggiungere demand generation?}}

**Informazioni mancanti per migliorare:** {{MISSING_INFO — dati di conversione reali per sostituire le ipotesi; valore medio reale di un cliente}}.
