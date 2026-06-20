> **EN —** Engagement Radar (daily): opens Chrome on LinkedIn, finds fresh on-target posts worth commenting on, and returns link + recap + an angle in your voice. Read-only — it never writes or posts comments. · suggested cadence: weekdays 08:00 (Mon–Fri)
> **IT —** Engagement Radar (giornaliero): apre Chrome su LinkedIn, cerca post freschi in target su cui commentare e restituisce link + recap + un angolo nella tua voce. Solo lettura — non scrive né pubblica commenti. · cadenza suggerita: giorni feriali 08:00 (lun–ven)

---
**Suggested schedule (cron):** `0 8 * * 1-5`
**Prompt:**

Esegui l'**Engagement Radar giornaliero** per il profilo LinkedIn di {{FOUNDER}} (progetto "{{COMPANY}}", cartella `linkedin/`). Obiettivo: dargli ogni mattina una rosa di post in target su cui commentare, con **link + recap + angolo**. **NON scrivere i commenti finiti e NON postare/commentare/inviare nulla** — solo leggere e proporre. Il commento lo scrive {{FOUNDER}}.

STRUMENTO: usa **Claude in Chrome** (tool `mcp__Claude_in_Chrome__*`: tabs_context_mcp, navigate, get_page_text, read_page) per navigare LinkedIn. Solo lettura.
- Se Chrome non è connesso / LinkedIn non è loggato / la pagina chiede login o captcha: **fermati e scrivi nel file che il run non è stato possibile** (non inventare post). Non tentare login.

CONTESTO (leggi prima):
- `linkedin/engagement_playbook.md` — §3.5 (ricerche salvate / Engagement Radar), §3.6 (**VOCE di {{FOUNDER}}**: valore + polarizzazione, contrarian, dati, sarcasmo sull'hype, domande taglienti; MAI accondiscendente, MAI pitch, MAI commento finito; rispetta i paletti di tono indicati nel playbook), §5 (Dream 30).
- `linkedin/reputation_engine.md` — Category Thesis e Theme.

PROCEDURA (in Chrome):
1. Apri 2-3 ricerche per argomento ordinate per "Più recenti" (da §3.5 A), es.:
   - https://www.linkedin.com/search/results/content/?keywords={{KEYWORD_QUERY_1}}&sortBy=%22date_posted%22
   - https://www.linkedin.com/search/results/content/?keywords={{KEYWORD_QUERY_2}}&sortBy=%22date_posted%22
   - https://www.linkedin.com/search/results/content/?keywords={{KEYWORD_QUERY_3}}&sortBy=%22date_posted%22
   Usa `get_page_text` per autori+testo e `read_page` (filter interactive) per estrarre i **link** (profilo/post).
2. Controlla l'attività recente di 2-3 **poster attivi in target** (ruotali ogni giorno), presi dalla tua People Map / Dream 30 in `engagement_playbook.md` — via `linkedin.com/in/<slug>/recent-activity/all/` (cerca lo slug se non lo conosci). Privilegia **persone**, non solo aziende.
3. Filtra via Category Thesis. Scegli **5-8 post freschi** (ultimi ~2 giorni) ad alto segnale: contrarian/hype da ribaltare, build reali, richieste/preventivi (lead), tesi su processi/dati/governance.

OUTPUT: scrivi `linkedin/engagement_radar/AAAA-MM-GG.md`. Per ogni post:
- **Autore (ruolo) + link** (al post se disponibile, altrimenti al profilo)
- **Recap** (1-2 righe)
- **Perché commentare** (reach / decisore in target / lead / tema)
- **Angolo per {{FOUNDER}}** (1 spunto NELLA SUA VOCE: contrarian/dato/domanda tagliente, valore + polarizzazione. NON il commento finito, NON accondiscendente, NON pitch, rispetta i paletti di tono.)

REGOLE: solo lettura (mai commentare/postare/connettere); non inventare (link reali visti in pagina); tono operatore. FINE: in chat, i 3 post migliori (autore + link + angolo) + nota se qualche ricerca non ha dato risultati utili.
