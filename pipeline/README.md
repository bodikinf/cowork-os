# Pipeline — il layer commerciale

> **EN —** The **sales layer** of cowork-os for people who run a CRM (e.g. Pipedrive). It holds the sales *rules* captured from the person, follow-up *templates* in their voice, and the *deal radar* output — and feeds the "Pipeline" section of the daily brief so they read one surface, not three. The CRM stays the source of truth on deal state; this folder holds the rules and the outputs, not a copy of the pipeline. Part of **cowork-os** by **Yempik**.
> **IT —** Il **layer commerciale** di cowork-os per chi lavora su un CRM (es. Pipedrive). Contiene le *regole* di vendita catturate dalla persona, i *template* di follow-up nella sua voce e l'output del *deal radar* — e alimenta la sezione "Pipeline" del daily brief, così la persona legge **una sola superficie**, non tre. Il CRM resta la fonte di verità sullo stato dei deal; qui vivono le regole e gli output, non una copia della pipeline.

---

## Perché esiste

Un commerciale non deve aprire tre schermate ogni mattina. Il principio è:

**Il deal radar è un motore di analisi (scrive un file). Il daily brief è l'unica superficie che la persona legge.** Il radar *alimenta* il brief.

```
CRM (Pipedrive, live)
      │  il task pipeline-deal-radar legge i deal e applica pipeline/rules.md
      ▼
pipeline/deal_radar.md   (scaduti · fermi · da sistemare)
      │  il founder-daily-brief tira su i top item
      ▼
📥 Daily brief  →  UNA lettura al mattino
```

La skill `pipeline-followup` è **on-demand**: quando serve, prende un deal senza risposta da N giorni, legge il thread Gmail e prepara una **bozza** (draft-only) — non è una routine che gira da sola.

## I file

| File | Contiene | Chi lo scrive |
|---|---|---|
| `rules.md` | Regole del processo di vendita: stadi reali, cosa è "fermo", soglia no-reply, campi usati, criteri di priorità. | La `knowledge-transfer` skill, in sessione con la persona. Poi si corregge a mano. |
| `deal_radar.md` | Output del radar: deal con follow-up scaduto, deal fermi, deal da sistemare. Datato, sovrascritto a ogni run. | Il task `pipeline-deal-radar` (o on-demand). |
| `followup_templates.md` | Template di follow-up nella voce della persona, per tipo di situazione. | La KT + rifinitura a mano. |

## Regola d'oro sui dati

- Il **CRM è la fonte di verità** sullo stato dei deal. Il radar **legge**, non scrive nel CRM (salvo, se deciso, aggiungere una *nota* o un'*attività* — mai spostare stadi in autonomia).
- Le automazioni **leggono `rules.md`**: non hardcodare soglie o stadi nei prompt. Cambi le regole → cambia il comportamento.
- Niente nomi di clienti reali, importi o accessi in file versionati pubblicamente. Tieni `pipeline/` fuori dal repo pubblico se contiene dati reali (vedi `.gitignore`: sezione "Your real content").

## Connettori richiesti

- **Pipedrive** (o altro CRM) *(lettura)* — per il deal radar e la skill di follow-up. MCP da installare nel progetto Cowork.
- **Gmail** *(lettura + bozze)* — la skill `pipeline-followup` legge il thread e crea la **bozza** (non invia).

> Se il CRM non è collegato, il radar non fallisce: scrive "fonte CRM non disponibile" e si ferma, senza inventare deal.
