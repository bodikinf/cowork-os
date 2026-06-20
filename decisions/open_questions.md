> **EN —** Open questions, hypotheses to validate, and blockers. When one closes, log the decision in `decisions_log.md` and mark the item resolved (don't delete it).
> **IT —** Domande aperte, ipotesi da validare e bloccanti. Quando una si chiude, registra la decisione in `decisions_log.md` e marca la voce come risolta (non eliminarla).

---

# {{COMPANY}} — Domande aperte & ipotesi da validare

> Cose non ancora decise, non chiare, o assunte. Le decisioni prese stanno in `decisions_log.md`.

## Formato di una voce
> Raggruppa per area. Usa un'icona di stato e marca le voci risolte invece di cancellarle.
> 🔴 bloccante · 🟠 importante · 🟡 da chiarire · 🟢 opportunità · ✅ risolto · ~~barrato~~ superato.

```
- 🟡 **{{DOMANDA / IPOTESI}}** — {{contesto}}. **Da decidere:** {{le opzioni}}. *{{nuova, DATE}}*
```

Quando si chiude:
```
- ✅ **{{DOMANDA}}** — **RISOLTO ({{DATE}}):** {{esito}}. → registrata in `decisions_log.md` #{{N}}.
```

## Setup tecnico (bloccanti operativi)
- 🔴 **{{BLOCCANTE_TECNICO}}** — {{contesto}}. **Da decidere:** {{opzioni}}. *{{nuova, DATE}}*

## CRM / gestione lead
- 🟠 **{{DOMANDA_CRM}}** — {{contesto}}.

## Contenuti / prova
- 🟡 **{{DOMANDA_CONTENUTI}}** — {{contesto}}.

## Strategia (scelte non ancora prese)
- 🟢 **{{IPOTESI_STRATEGICA}}** — {{contesto}}.

## Ipotesi esplicite da validare con dati reali
- **{{IPOTESI}}** — è una stima, non un dato storico.

## Da completare / domande per il fondatore
- {{DOMANDA_PER_FONDATORE}}.

> **Nota di metodo:** questo file è anche dove finiscono le note "esplorative" su nuovi prodotti/offerte prima che diventino workstream. Quando un'esplorazione diventa reale, promuovila a `products/<nome>/` o `business-development/` e logga la decisione. Tieni **fuori** da un file pubblico: nomi di lead/clienti reali, importi reali, accessi/credenziali, dettagli di deliverable di clienti.
