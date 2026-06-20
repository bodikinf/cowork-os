> **EN —** Trend Hunter for LinkedIn: twice a week scans web/RSS + X (twitterapi-io), filters everything through your Category Thesis, and outputs emerging trends + post ideas. Has a strict read-budget cap. · suggested cadence: Mondays (full) + Thursdays (light pulse)
> **IT —** Trend Hunter per LinkedIn: 2×/settimana analizza web/RSS + X (twitterapi-io), filtra tutto attraverso la tua Category Thesis e produce trend emergenti + idee post. Ha un tetto rigoroso di letture. · cadenza suggerita: lunedì (completo) + giovedì (pulse leggero)

---
**Suggested schedule (cron):** `0 7 * * 1,4`
**Prompt:**

Esegui il **Trend Hunter** per il profilo LinkedIn di {{FOUNDER}} (progetto "{{COMPANY}}", cartella `linkedin/`). Ogni run parte da zero: segui questi passi.

MODALITÀ (in base al giorno della settimana):
- **Lunedì = run COMPLETO** (web/RSS + X + People Map + comment mining).
- **Giovedì = PULSE leggero**: solo trend X + ricerca web veloce, output con 3 idee per il post del giorno seguente. Salta People Map e comment mining.

CONTESTO (leggi prima questi file):
- `linkedin/reputation_engine.md` — Category Thesis, tassonomia Theme/Format, §7 People Map, §8 Trend Hunter, §9 Comment Mining, §10 KPI Hierarchy.
- `linkedin/content_engine.md` — la idea bank (per NON proporre doppioni).
- `linkedin/trend_hunter/README.md` e l'ultimo report in `linkedin/trend_hunter/` (continuità).

BUDGET (rispettalo rigorosamente): twitterapi.io è a consumo (~$0,00015 a tweet letto). **Tetto: ~400 letture X il lunedì, ~150 il giovedì.** Meglio poche query mirate che tante generiche.

FONTI:
A) Web/RSS: ricerche web mirate + le testate di settore che segui (es. MarkTechPost, The Batch, Import AI, Ahead of AI, Hugging Face blog, OpenAI news).
B) X — tool MCP `twitterapi-io`. NOTE TECNICHE VERIFICATE (rispettale):
   - `search_tweets`: il segnale vero è qui. Usa **query semplici** (in italiano rendono molto: es. "{{KEYWORD_IT_1}}", "{{KEYWORD_IT_2}}"; in inglese "{{KEYWORD_EN_1}}", "{{KEYWORD_EN_2}}"). EVITA combinazioni con molti operatori + min_faves (tornano vuote). queryType "Latest" o "Top".
   - `get_tweet_replies`: usa **SEMPRE `queryType: "Latest"`** (Top → errore API; Likes → errore wrapper).
   - `get_trends`: i trending topic globali (woeid 1) sono spesso rumore (sport/intrattenimento) → usali solo se pertinenti, NON come fonte primaria.
   - **Gli output X sono enormi** (spesso >150k caratteri e vengono salvati su file): NON ingerirli interi. Distilla solo i campi utili: `text`, `author.userName`, `likeCount`, `viewCount`, `id`. Se un risultato eccede, leggine una porzione/usane un estratto — non rileggere tutto.
   - Solo lunedì: `get_user_last_tweets` su 8-10 voci chiave (People Map in `reputation_engine.md` §7) per temi/pain/linguaggio; e `get_tweet_replies` per il COMMENT MINING **su thread {{ICP}} rilevanti** (post di aziende/founder in target sul tuo tema), NON su annunci-hype globali (es. lanci modello dei big) che danno solo rumore.

FILTRO: passa TUTTO attraverso la tua Category Thesis (la tesi di categoria definita in `reputation_engine.md`): per ogni trend chiediti cosa significa per la categoria mentale che vuoi possedere ({{CATEGORY}}). Scarta il rumore.

OUTPUT: scrivi un file NUOVO in `linkedin/trend_hunter/` chiamato con la data odierna (`AAAA-MM-GG.md`) con:
1) Trend emergenti (con fonte/link) 2) Trend saturi 3) Opportunità poco presidiate 4) Idee post (ognuna con Theme + Format + hook) 5) Proposte per la idea bank (righe: ID, Idea, Theme, Format, Fonte) 6) [SOLO lunedì] Proposte People Map (account + perché) + insight Comment Mining (obiezioni/linguaggio reali). NON modificare i file core (`content_engine.md`, `reputation_engine.md`) in automatico: solo proposte da approvare.

REGOLE: non inventare dati, cita sempre le fonti; tono operatore, concreto, niente hype; resta entro il tetto di letture.

FINE: dichiara il percorso del file salvato, elenca in chat le 3 idee post migliori (Theme × Format + hook) e indica il numero stimato di letture X usate nel run.
