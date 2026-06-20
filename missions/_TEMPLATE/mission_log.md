# Mission Log — Evidence Log

> **EN —** A dated, append-only record of every meaningful action: what you did, to whom, the result, and the next step. It exists to stop loops — so you never re-try a dead end or forget what was already attempted. Append new entries; never rewrite history.
> **IT —** Un registro datato e in sola aggiunta di ogni azione rilevante: cosa hai fatto, verso chi, l'esito e il next step. Serve a fermare i loop — così non ritenti mai un vicolo cieco né dimentichi cosa è già stato provato. Aggiungi voci nuove; non riscrivere la storia.

> Ogni azione importante documentata, per evitare loop e capire cosa è già stato tentato.

## Tabella sintetica

| Data | Route | Azione | Target | Stato | Risultato | Next step | Note |
|------|-------|--------|--------|-------|-----------|-----------|------|
| {{DATE}} | {{ROUTE}} | {{ACTION}} | {{TARGET}} | {{STATUS}} | {{RESULT}} | {{NEXT_STEP}} | {{NOTES}} |
| {{DATE}} | {{ROUTE}} | {{ACTION}} | {{TARGET}} | {{STATUS}} | {{RESULT}} | {{NEXT_STEP}} | {{NOTES}} |

> Stati ammessi: `todo` · `in corso` · `done` · `partial` · `bloccato` · `WIN` · `scartata`.
> Per `{{TARGET}}` usa ruoli o `{{PLACEHOLDER}}`, **mai** nomi reali di persone/aziende in un repo condiviso.

---

## Registro esteso (per azioni che meritano contesto)

Per le azioni complesse usa il blocco YAML qui sotto: regge testo lungo nel campo `result` senza rompere la tabella.

```yaml
- date: {{DATE}}
  route: {{ROUTE}}
  action: {{ACTION}}
  target: {{TARGET}}
  status: {{STATUS}}     # done | partial | bloccato | WIN | scartata
  result: >
    {{RESULT_MULTILINE}}
  next_step: {{NEXT_STEP}}
  notes: {{NOTES}}        # es. "bozze non approvate", "nessun invio fatto", "boundary: non eseguo login al posto dell'utente"

- date: {{DATE}}
  route: {{ROUTE}}
  action: {{ACTION}}
  target: {{TARGET}}
  status: {{STATUS}}
  result: >
    {{RESULT_MULTILINE}}
  next_step: {{NEXT_STEP}}
  notes: {{NOTES}}
```

> **Buone pratiche di log**
> - Registra anche i **non-invii** e i **boundary** (es. "pitch non inviato di proposito: proof of work non ancora pubblico"). Il log deve dire anche cosa **non** hai fatto e perché.
> - Quando una route diventa `WIN` o `scartata`, riportalo anche in `route_map.md` (sezione *Aggiornamento route*).
> - Annota la **fonte** quando registri un fatto di intelligence, così resta verificabile.
