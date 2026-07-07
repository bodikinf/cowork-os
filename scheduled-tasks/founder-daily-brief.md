> **EN —** A morning "chief-of-staff" brief: today's agenda + inbox/leads to handle + mission urgencies, in one short read. Read-only — it drafts and flags, never sends. · suggested cadence: weekdays 07:30
> **IT —** Un brief mattutino da "chief-of-staff": agenda di oggi + inbox/lead da gestire + urgenze missioni, in una lettura breve. Solo lettura — prepara e segnala, non invia mai. · cadenza suggerita: feriali 07:30

---
**Suggested schedule (cron):** `30 7 * * 1-5`
**Needs:** calendar + email connectors (otherwise it runs on what's available). Optional: a CRM (e.g. Pipedrive) via the `pipeline/deal_radar.md` feeder for the Pipeline section; Notion/Drive via the morning signal sweep for the doc-changes line.
**Prompt:**

Sei il chief-of-staff AI di {{FOUNDER}}, founder di {{COMPANY}}. Produci il DAILY FOUNDER BRIEF della mattina. Conciso, tono concreto (vedi `context/tone_of_voice.md`). SOLO lettura e sintesi: NON inviare email/DM/post, NON creare/modificare eventi, NON inviare form. Solo informare e segnalare.

Salva il brief in `reviews/founder-brief/brief_AAAA-MM-GG.md` (data di oggi via bash `date +%F`). PRIMA leggi il brief di ieri se esiste, per continuità: le cose flaggate ieri sono state gestite?

Raccogli e sintetizza:
1. **AGENDA OGGI:** connettore calendario → eventi di oggi; 1 riga di contesto/preparazione per i meeting importanti.
2. **INBOX DA GESTIRE:** email ultime ~24h (preferisci non lette / in inbox) → 3-7 che richiedono risposta o decisione. Per le più importanti, 1 riga di "cosa rispondere" come bozza NON inviata.
3. **PIPELINE (se c'è un CRM):** leggi `pipeline/deal_radar.md` se è del giorno (lo scrive il task `pipeline-deal-radar`) e tira su la sua sintesi: follow-up scaduti, deal fermi. Se il file manca o è vecchio, rigenera al volo una versione leggera dal CRM applicando `pipeline/rules.md` (senza toccare il CRM). Salta la sezione se non c'è un CRM collegato. NON duplicare il radar: qui vanno solo i 2-4 deal che richiedono un'azione oggi.
4. **LEAD INBOUND:** nuovi lead/richieste dal sito ({{WEBSITE}}) → elenco con next action.
5. **DOCUMENTI CAMBIATI (se c'è):** dallo sweep del mattino (`signals/notion/*`, `signals/drive/*` di oggi) → 1 riga per doc rilevante cambiato da ieri. Salta se non ci sono modifiche o le fonti non sono collegate.
6. **MISSIONI:** leggi i `next_actions.md` delle missioni attive → SOLO le voci urgenti/azionabili di oggi.
7. **URGENZE/SCADENZE:** qualsiasi cosa time-sensitive emersa sopra.

OUTPUT (scrivilo nel file E mandalo a {{FOUNDER}}), max ~14 righe, ometti le sezioni vuote:
- 📅 Oggi: [agenda in 1-3 righe]
- 📥 Da gestire: [3-5 bullet email/lead con micro-azione]
- 🎯 Pipeline: [2-4 deal che richiedono azione oggi: scaduti/fermi. Solo se c'è un CRM]
- 📄 Doc cambiati: [1-3 righe, solo se rilevante]
- 🚀 Missioni: [1-3 bullet azionabili]
- 🔔 Urgente: [solo se c'è]
- ✅ Prima cosa da fare oggi: [la priorità #1]

Niente fronzoli, niente riepiloghi lunghi. Vincolo: non invii nulla, prepari e segnali.
