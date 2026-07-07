> **EN —** Workspace maintenance: audits the knowledge base for unsaved decisions, untracked questions, duplicates, stale info and source conflicts, then proposes fixes (never deletes history). · suggested cadence: 1st & 15th of each month, 15:00
> **IT —** Manutenzione workspace: controlla la knowledge base per decisioni non salvate, domande non tracciate, duplicati, informazioni obsolete e conflitti tra fonti, e propone correzioni (non cancella mai lo storico). · cadenza suggerita: il 1 e il 15 di ogni mese, 15:00

---
**Suggested schedule (cron):** `0 15 1,15 * *`
**Prompt:**

Esegui una Workspace Maintenance Review per {{COMPANY}} (Project Cowork "{{COMPANY}}").

Agisci come knowledge manager del Project {{COMPANY}}.

Scopri PRIMA la struttura reale (non assumere un set fisso di cartelle — ogni installazione è diversa):
- elenca le cartelle top-level del workspace (directory listing via bash `ls`) **e/o** leggi `PROJECT_STRUCTURE.md`, che è il **manifesto** dei moduli di questo workspace;
- audita OGNI modulo effettivamente presente (possono esserci `context/`, `marketing/`, `website/`, `decisions/`, `signals/`, `reviews/`, `products/`, `missions/`, e qualsiasi **modulo custom** creato per questo cliente, es. `clients/`);
- salta senza allarmismi i moduli assenti (non segnalarli come "mancanti");
- se trovi una cartella-modulo **non registrata** in `PROJECT_STRUCTURE.md`, segnalala e proponi di registrarla (il manifesto deve restare in sync).

Obiettivo: verificare che la knowledge base di {{COMPANY}} sia aggiornata, coerente e utilizzabile.

Cerca:
- decisioni non salvate;
- domande aperte non tracciate;
- ipotesi non validate;
- task sito non inseriti nel backlog;
- insight marketing non salvati;
- dati o report non archiviati;
- contenuti duplicati;
- informazioni obsolete;
- conflitti tra fonti;
- file vuoti o inutili.

Output richiesto:
1. stato della knowledge base;
2. file aggiornati;
3. incoerenze trovate;
4. duplicazioni trovate;
5. informazioni obsolete;
6. decisioni/domande/ipotesi/task aggiunti;
7. changelog sintetico;
8. raccomandazioni per mantenere ordine.

Regole:
- non inventare informazioni;
- non cancellare decisioni storiche;
- se trovi conflitti, segnalali;
- mantieni i file sintetici e operativi;
- termina con `Memory Update` nel formato standard del Project.
