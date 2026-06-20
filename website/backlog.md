> **EN —** Concrete, prioritized tasks on the live site. One entry per task. Update as you add/close work. The current site architecture lives in `website_notes.md`.
> **IT —** Task concreti e prioritizzati sul sito in produzione. Una voce per task. Aggiornalo man mano che apri/chiudi lavoro. Lo stato dell'architettura è in `website_notes.md`.

---

# {{COMPANY}} — Backlog Sito

> Task concreti sul sito (`{{WEBSITE_REPO}}`). Lo stato attuale dell'architettura è in `website_notes.md`.
> Convenzione: ogni task ha priorità **[ALTA] / [MEDIA] / [BASSA]** e l'**obiettivo commerciale** a cui è legato.

## Formato di una voce backlog

```
- [ ] **[ALTA|MEDIA|BASSA] {{TITOLO}}** *(area: Copy/SEO/UX/Conversione/Tecnico)* — {{descrizione concreta}}.
  **Motivo:** {{perché conta, legato a un obiettivo commerciale}}.
  **Fatto quando:** {{criterio di completamento osservabile}}.
```

Stati: `[ ]` da fare · `[~]` in corso · `[x]` fatto.

---

## Priorità ALTA — superficie commerciale che converte
> Qui vanno i task con ROI più alto: di solito, portare in organico la domanda che oggi paghi in paid sui cluster che chiudono.

- [ ] **[ALTA] {{TASK_ALTA_1}}** *(SEO/Conversione)* — {{descrizione}}.
  **Motivo:** {{...}}. **Fatto quando:** {{...}}.

## Priorità MEDIA — coerenza, conversione, link interni
- [ ] **[MEDIA] {{TASK_MEDIA_1}}** *(Coerenza)* — {{descrizione}}.
  **Motivo:** {{...}}. **Fatto quando:** {{...}}.

## Priorità BASSA — rifiniture e GEO
- [ ] **[BASSA] {{TASK_BASSA_1}}** *(Tecnico/GEO)* — {{descrizione}}.

## Già risolto (storico, non cancellare)
- [x] {{TASK_CHIUSO}} — {{cosa è stato fatto}}.
