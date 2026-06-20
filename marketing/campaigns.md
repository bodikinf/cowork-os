> **EN —** How campaigns are structured and managed (the execution layer). One entry per campaign. The *why* of the clusters lives in `strategy.md`; ad copy in `content.md`.
> **IT —** Come le campagne sono strutturate e gestite (il livello esecutivo). Una voce per campagna. Il *perché* dei cluster sta in `strategy.md`; i testi degli annunci in `content.md`.

---

# {{COMPANY}} — Campagne ({{CHANNEL}})

> Convenzione: ogni campagna è una voce con lo stesso formato. Lo **stato** in cima (attiva / in pausa / chiusa) e la data dell'ultimo aggiornamento. I dati di performance datati vanno in `monitoraggio/monitoraggio_adv_YYYY-MM-DD.md`, non qui.

## Formato di una voce campagna

```
### {{NOME_CAMPAGNA}} — {{STATO: attiva | in pausa | chiusa}} (agg. {{DATE}})
- **Canale / tipo:** {{es. Search · obiettivo "Lead"}}
- **Budget:** {{AMOUNT}}/giorno · **Località:** {{...}} · **Lingua:** {{...}}
- **Struttura:** {{n. gruppi di annunci}} gruppi, ciascuno con keyword stretta, tutti verso {{landing}}
- **Bidding:** {{strategia attuale}} → {{prossima soglia}}
- **Conversioni:** primaria = {{...}}; secondarie = {{...}}
- **KPI di riferimento:** {{CTR}} · {{tasso conv.}} · {{CPL/CPA target}}
- **Stato/insight più recente:** {{1–2 righe, con `[illustrativo]` al posto dei numeri reali}}
- **Da completare:** {{azioni aperte}}
```

## Impostazioni base (checklist di lancio, riutilizzabile)
- **Tipo:** una sola campagna Search, obiettivo "Lead". Niente Performance Max / campagne intelligenti con budget piccolo e lead B2B.
- **Budget:** {{AMOUNT}}/giorno, concentrato sulla campagna commerciale.
- **Località:** {{MARKET}}, opzione **"Presenza"** (non "presenza o interesse", per evitare clic dall'estero).
- **Reti:** Display e Partner di ricerca **DISATTIVATI** (default attivi: su B2B bruciano budget).

## Negative keyword (lista a livello account)
> Parti da una lista anti-spazzatura e ampliala rivedendo il rapporto "Termini di ricerca" ogni 2–3 giorni.
`gratis · gratuito · free · corso · corsi · tutorial · significato · cos'è · come funziona · esempi · python · github · open source · download · pdf · wikipedia · login · studenti · tesi · università · stage · lavoro · stipendio · {{ALTRE_NEGATIVE_DI_DOMINIO}}`

## Strategia di offerta (bidding) — roadmap generica
| Fase | Quando | Strategia |
|---|---|---|
| Avvio | Sett. 1–3 (0 conversioni) | CPC manuale (o "Massimizza clic" con tetto CPC) |
| Crescita | Da ~15–20 conv./mese | Massimizza conversioni |
| Maturità | 30+ conv./mese | CPA target |

## Da completare
- {{OPEN_ITEM — es. confermare i tetti CPC impostati; correggere eventuali gruppi senza annunci}}
