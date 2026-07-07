# Decision candidates — in attesa di conferma

> **EN —** The **inbox for decisions**. The signal sweeps drop here anything that *looks like* a decision or commitment detected in email/Slack. Nothing here is authoritative yet — a candidate becomes a real decision only when a human confirms it in the **Decision Radar**. This gate is what prevents the brain from being poisoned by half-decisions and misreadings.
> **IT —** L'**inbox delle decisioni**. Gli sweep ci mettono tutto ciò che *sembra* una decisione o un impegno rilevato in email/Slack. Qui niente è ancora ufficiale: un candidate diventa decisione vera solo quando un umano lo conferma nel **Decision Radar**. Questo gate evita che il brain venga inquinato da mezze-decisioni e letture sbagliate.

---

## Flusso

```
signal (decision|commitment)  →  candidate [proposed]  →  [conferma umana nel Radar]
    ├─ confermato   →  active_decisions.md  +  decisions_log.md   (status: active)
    ├─ scartato     →  status: rejected     (resta qui come storico, non si cancella)
    └─ non chiaro   →  open_questions.md     (serve altra info)
```

## Schema decisione (usato qui, in `active_decisions.md` e nel log)

Obbligatori: **status**, **owner**, **review**. Il resto è opzionale (Claude lo inferisce dove può, senza inventare).

```
### D-{{NNN}} · {{titolo breve della decisione}}
- status: proposed        # proposed | active | superseded | expired | rejected | needs-review
- owner: {{chi}}          # chi possiede/decide
- review: {{AAAA-MM-GG}}  # quando va ri-verificata
- date: {{AAAA-MM-GG}}    # quando (sembra) presa
- confidence: {{low|medium|high}}
- decision: {{cosa si è deciso, 1 frase}}
- why: {{motivo, se noto}}
- reversal: {{condizione che farebbe rivedere la decisione}}
- source: {{email di X / #canale / call — link o ID se c'è}}
- linked: {{file collegati, es. context/positioning.md}}
```

> Regola cattura: tieni i candidate **leggeri**. Meglio 6 campi veri che 10 inventati. Se `owner`/`review` non sono deducibili, lascia `{{—}}` e segnalalo nel Radar come "candidate incompleto".

---

## Candidates aperti

> Gli sweep appendono qui sotto. Il Decision Radar li processa e li marca `active` / `rejected` / li manda in `open_questions`.

<!-- esempio (rimuovi):
### D-007 · Pricing Company Brain Starter a 4.500€
- status: proposed
- owner: {{—}}
- review: 2026-08-07
- date: 2026-07-07
- confidence: medium
- decision: listino setup a 4.500€ per il segmento 1-10 persone
- source: email inviata a un prospect, 2026-07-07
- linked: (da collegare)
-->

_(nessun candidate — gli sweep lo popolano)_
