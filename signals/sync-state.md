# Sync state — watermark

> **EN —** Idempotency watermark for the signal sweeps. Each source records the **last processed item** so AM/PM runs and re-runs never double-capture. Contains only timestamps/IDs — **no message content**. Safe to commit.
> **IT —** Watermark di idempotenza per gli sweep. Ogni fonte registra l'**ultimo elemento processato** così le run AM/PM e i rerun non catturano due volte. Contiene solo timestamp/ID — **nessun contenuto**. Committabile.

---

> Regola per Claude: **prima** di uno sweep, leggi il watermark della fonte e processa solo elementi **più recenti**. **Dopo** lo sweep, aggiorna il watermark. Se un watermark è vuoto (primo run), processa le ultime 24h e inizializzalo.

## email

- `last_processed_at`: {{—}}   <!-- ISO 8601, es. 2026-07-07T18:00:00+02:00 -->
- `last_thread_id`: {{—}}
- `note`: {{—}}

## slack

- `last_processed_at`: {{—}}
- `last_ts`: {{—}}            <!-- ultimo message ts processato -->
- `channels_watched`: {{—}}  <!-- es. #general, #sales, #product -->
- `note`: {{—}}

## notion

- `last_processed_at`: {{—}}   <!-- ISO 8601: ultimo edit time processato -->
- `pages_watched`: {{—}}       <!-- ID o nomi delle pagine/DB da osservare (es. "Playbook vendite", "Note pipeline") -->
- `note`: {{—}}                <!-- se vuoto: chiedi quali 3-6 pagine/DB osservare; NON leggere tutto Notion -->

## gdrive

- `last_processed_at`: {{—}}   <!-- ISO 8601: ultimo modifiedTime processato -->
- `folders_watched`: {{—}}     <!-- ID o percorsi delle cartelle da osservare (es. "Proposte", "Contratti") -->
- `note`: {{—}}                <!-- se vuoto: chiedi quali cartelle osservare; NON scansionare tutto il Drive -->

## run log (append, 1 riga per run)

| Run | Fonte | Fino a (watermark) | Nuovi signal | Candidate creati | Note |
|---|---|---|---|---|---|
| _es. 2026-07-07 AM_ | email | 2026-07-07T07:30 | 0 | 0 | init |
