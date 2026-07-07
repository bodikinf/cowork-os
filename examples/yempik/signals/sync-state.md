# Sync state — watermark (esempio compilato)

> **EN —** Filled example (sanitized) of the sweep watermark. Only timestamps/IDs — no content.
> **IT —** Esempio compilato (sanitizzato) del watermark degli sweep. Solo timestamp/ID — nessun contenuto.

---

## email
- `last_processed_at`: 2026-06-15T18:00:00+02:00
- `last_thread_id`: thr_[illustrativo]
- `note`: inviate + ricevute, ok

## slack
- `last_processed_at`: 2026-06-15T18:00:00+02:00
- `last_ts`: 1718467200.000100
- `channels_watched`: #commerciale, #marketing, #prodotto, #general
- `note`: #general tenuto solo per contesto (alto rumore)

## run log

| Run | Fonte | Fino a (watermark) | Nuovi signal | Candidate creati | Note |
|---|---|---|---|---|---|
| 2026-06-15 AM | email | 2026-06-15T07:30 | 3 | 1 | — |
| 2026-06-15 AM | slack | 2026-06-15T07:30 | 5 | 1 | #general troncato (catch-up) |
| 2026-06-15 PM | email | 2026-06-15T18:00 | 2 | 1 | listino prospect |
| 2026-06-15 PM | slack | 2026-06-15T18:00 | 4 | 0 | 2 scartati (rumore) |
