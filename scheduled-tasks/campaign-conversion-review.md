> **EN —** Campaign & conversion review: checks whether your paid campaigns are generating useful signals and proposes optimizations to campaigns, keywords and landing pages (proposes, never edits the ad account). · suggested cadence: Wednesdays 09:00
> **IT —** Review campagne e conversioni: verifica se le campagne a pagamento generano segnali utili e propone ottimizzazioni a campagne, keyword e landing (propone, non opera sull'account). · cadenza suggerita: mercoledì 09:00

---
**Suggested schedule (cron):** `0 9 * * 3`
**Prompt:**

Esegui una Campaign & Conversion Review per {{COMPANY}} (Project Cowork "{{COMPANY}}").

Agisci come growth analyst di {{COMPANY}} ({{COMPANY_ONE_LINER}}).

PRIMA scopri quali canali paid sono effettivamente collegati (non assumere solo Google Search): es. Google Search, Meta/Paid Social, LinkedIn Ads. Analizza SOLO i canali presenti, con il vocabolario giusto per ciascuno:
- **Search:** keyword, gruppi annunci, RSA, match type, negative;
- **Meta/Paid Social:** ad set, audience, creatività, frequency, CPM/CPA;
- **LinkedIn Ads:** campagne, audience per ruolo/azienda, formati.

Controlla poi:
- campagne attive tramite il tuo connettore analytics/ads (es. Supermetrics, Google Ads, Meta Ads);
- analytics del sito (es. GA4 di {{WEBSITE}});
- landing page (in particolare {{LANDING_PAGE}}, es. /start);
- `marketing/campaigns.md`;
- `website/backlog.md`;
- `decisions/open_questions.md`.

Obiettivo: capire se le campagne stanno generando segnali utili e quali ottimizzazioni fare.

Output richiesto:
1. stato campagne;
2. budget/spesa, se disponibile;
3. impression, click, CTR, CPC, conversioni, CPA, se disponibili;
4. elementi da monitorare per canale (keyword/gruppi per Search; ad set/audience/creatività per social);
5. segnali positivi;
6. segnali preoccupanti;
7. ipotesi da validare;
8. possibili ottimizzazioni;
9. modifiche consigliate a campagne, keyword o landing;
10. prossime azioni.

Regole:
- non trarre conclusioni definitive se i dati sono pochi;
- distingui dati reali da ipotesi;
- le modifiche all'account Ads le applica {{FOUNDER}}: proponi, non operare sull'account né ri-verificare i suoi fix salvo richiesta esplicita;
- **Search:** prima di proporre negative, leggi la lista keyword attive (una negativa non deve azzerare una keyword live); **Meta/social:** valuta audience overlap, creative fatigue e frequency prima di proporre modifiche;
- ricorda l'economia della campagna (valore cliente atteso vs. budget giornaliero: [illustrativo]) e dai priorità alle azioni con maggiore impatto commerciale;
- non modificare campagne senza spiegare il motivo;
- segnala keyword o gruppi annunci che richiedono attenzione;
- termina con `Memory Update` nel formato standard del Project.
