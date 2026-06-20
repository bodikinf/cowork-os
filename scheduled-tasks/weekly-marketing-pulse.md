> **EN —** Weekly marketing pulse: reads live analytics + ad campaigns + your marketing/website memory files and returns the week's priorities and 5 recommended actions. · suggested cadence: Mondays 08:00
> **IT —** Pulse marketing settimanale: legge analytics e campagne live + i file di memoria marketing/sito e restituisce le priorità della settimana e 5 azioni consigliate. · cadenza suggerita: lunedì 08:00

---
**Suggested schedule (cron):** `0 8 * * 1`
**Prompt:**

Esegui una Weekly Marketing Pulse per {{COMPANY}} (Project Cowork "{{COMPANY}}").

Agisci come marketing strategist, growth analyst e communication partner di {{COMPANY}} ({{COMPANY_ONE_LINER}}).

Controlla:
- analytics e campagne live (es. Supermetrics → campagne attive, GA4 di {{WEBSITE}}, Keyword Planner, Google Trends);
- `marketing/strategy.md`;
- `marketing/campaigns.md`;
- `marketing/content.md`;
- `website/website_notes.md`;
- `website/backlog.md`;
- `decisions/decisions_log.md`;
- `decisions/open_questions.md`.

Obiettivo: produrre una review sintetica e operativa dello stato marketing di {{COMPANY}} e indicare le priorità della settimana.

Output richiesto:
1. executive summary;
2. dati o segnali più importanti;
3. performance campagne;
4. insight analytics ({{KPI_1}}, conversioni, ecc.);
5. keyword o trend rilevanti;
6. problemi o opportunità sul sito;
7. decisioni o domande aperte rilevanti;
8. priorità marketing della settimana;
9. 5 azioni consigliate;
10. file aggiornati o da aggiornare.

Regole:
- non inventare dati;
- cita sempre le fonti usate;
- separa fatti, ipotesi e raccomandazioni;
- dai priorità alle azioni con maggiore impatto commerciale;
- tieni conto dei limiti noti del tracking del tuo setup (es. analytics in differita, conversioni Ads confermate via notifica): non flaggare come bug ciò che è un comportamento atteso e già documentato;
- se i dati sono insufficienti, dichiaralo chiaramente;
- termina con `Memory Update` nel formato standard del Project (File aggiornati, Decisioni, Domande aperte, Ipotesi, Task, Rischi, Opportunità, Prossime azioni).
