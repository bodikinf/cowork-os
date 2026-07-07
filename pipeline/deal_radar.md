# Deal Radar — {{COMPANY}}

> Output rigenerato dal task `pipeline-deal-radar` (o on-demand: *"fammi il deal radar"*). Sovrascritto a ogni run. Legge il CRM live + `pipeline/rules.md`. Read-only sul CRM: segnala, non modifica. I top item di questo file entrano nella sezione "🎯 Pipeline" del `founder-daily-brief`.

**Ultimo aggiornamento:** {{DATA-ORA}} · **Deal analizzati:** {{N}} · **Fonte:** {{CRM}}

---

## 🔴 Follow-up scaduti (silenzio oltre soglia)
> Deal senza risposta oltre la soglia in `rules.md`. Candidati alla skill `pipeline-followup`.

| Deal | Stadio | Ultimo contatto | Giorni di silenzio | Prossima azione suggerita |
|---|---|---|---|---|
| {{—}} | {{—}} | {{—}} | {{—}} | {{—}} |

## 🟠 Deal fermi (nessuna attività / azione mancante)
> In stadio avanzato ma senza prossima attività o data. Rischio #1: thread caldo dimenticato.

| Deal | Stadio | Fermo da | Cosa manca |
|---|---|---|---|
| {{—}} | {{—}} | {{—}} | {{—}} |

## 🟡 Da sistemare nel CRM (igiene)
> Deal senza owner, senza valore, stadio incoerente, dati da confermare. Non bloccano, ma sporcano il radar.

- {{—}}

## 🟢 In scadenza questa settimana (follow-up pianificati)
> Deal con data di follow-up entro 7 giorni: pronti, non in ritardo.

- {{—}}

---

**Sintesi per il brief (3 righe max):** {{es. "3 follow-up scaduti (top: {{deal}}), 2 deal fermi da sistemare, 4 follow-up pianificati questa settimana."}}
