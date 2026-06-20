# LinkedIn — Calendario editoriale

> **EN —** The weekly editorial calendar (3/week) and Theme rotation. Fill the "current week" tables at the start of each week. Update weekly.
> **IT —** Il calendario editoriale settimanale (3/sett) e la rotazione dei Theme. Compila le tabelle "settimana corrente" a inizio settimana. Aggiornare settimanalmente.

> ⚠️ **Esempi e occasioni illustrativi.** Sostituisci temi/occasioni col tuo settore (es. niente "milestone prodotto" se non hai un prodotto). · *Occasions/examples are illustrative — swap for your domain.*

> Cadenza e rotazione operativa. Razionale (cadenza, mix formati, finestre) in `strategy.md` §6. Metodo di produzione in `content_engine.md`. Tassonomia **Theme + Format** in `reputation_engine.md` §4.

## Ritmo settimanale fisso (3/sett)

| Giorno | Tipo editoriale | Format suggeriti | Obiettivo |
|--------|-----------------|------------------|-----------|
| **Lunedì** | Testo | Contrarian / Opinion / Story | Conversazione, voce grezza |
| **Mercoledì** | Carosello PDF | Framework / Case Study | Reach + profondità |
| **Venerdì** | Testo | Story / Error / Opinion | Conversazione, hook forte |

**Finestra:** pubblicare quando `{{FOUNDER}}` può presidiare i commenti ~60'. Default da testare: mattina `{{WINDOW_AM}}` (es. 7:30–9:00) o `{{WINDOW_LUNCH}}` (es. 12:30–13:30), feriali. Validare nel tracker.

## Rotazione Theme (per non sbilanciare)

Pesi target sui **Theme/pillar** (`reputation_engine.md` §4). Il tema madre — `{{PILLAR_1}}` — domina perché è il cuore della Category Thesis.

| Theme | Peso | Su ~12 post/mese |
|-------|------|------------------|
| `{{PILLAR_1}}` *(madre)* | ~40% | ~5 |
| `{{PILLAR_2}}` | ~25% | ~3 |
| `{{PILLAR_3}}` | ~20% | ~2-3 |
| `{{PILLAR_4}}` | ~10-15% | ~1-2 |

> Il **Format** ruota liberamente sul tema: lo stesso Theme può uscire come Story, Contrarian, Framework, ecc.

## Workflow di batch (consigliato)

1 sessione/settimana (~60-90') in cui `{{FOUNDER}}` + Claude:
1. pescano 3 idee dalla idea bank (1 per giorno, Theme bilanciati);
2. scrivono i 3 draft LinkedIn-first (`content_engine.md`);
3. passano checklist anti-articolo + Reputation Score + Association Test;
4. preparano caroselli/asset;
5. schedulano o tengono pronti i post.

## Pianificazione corrente

> **EN —** Plan the week here at the start of each week.
> **IT —** Compilare a inizio settimana.

### Settimana del `{{DATE}}` → `{{DATE}}`

| Giorno | Idea (ID) | Theme | Format | Tipo ed. | Stato | Note |
|--------|-----------|-------|--------|----------|-------|------|
| Lun `{{DATE}}` | `{{ID}}` | `{{PILLAR}}` | `{{FORMAT}}` | Testo | bozza / pronto / ✅ pubblicato | |
| Mer `{{DATE}}` | `{{ID}}` | `{{PILLAR}}` | `{{FORMAT}}` | Carosello | outline / pronto | |
| Ven `{{DATE}}` | `{{ID}}` | `{{PILLAR}}` | `{{FORMAT}}` | Testo | bozza / pronto | |

## Idee per occasioni / momenti

- Nuovo caso reale chiuso → Case Study / Story (Theme: `{{PILLAR_1}}`). **Mai** il nome del cliente: descrivi il settore.
- Edizione formazione in partenza → Theme adoption + CTA verso `{{SERVICE_2}}`.
- Milestone prodotto → Theme `{{PILLAR_2}}`, dietro le quinte.
- Notizia/uscita rilevante → **Opinion** sul Theme pertinente, **solo** se `{{FOUNDER}}` ha un take da operatore (non commento generico) — reinterpretato via Category Thesis.

---

> Un esempio compilato e sanitizzato di una settimana editoriale (Yempik) vive in `examples/yempik/linkedin/calendar.md`. Regola di anonimizzazione: nei file condivisi non vanno mai nomi di partner/clienti reali né ringraziamenti a persone nelle note — solo nel workspace privato.
