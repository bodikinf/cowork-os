# LinkedIn — Engagement Radar (digest giornaliero)

> **EN —** What the daily engagement-radar digest produces: a morning list of fresh, on-target posts worth commenting on — each with link + recap + why + an angle in your voice. **Claude does not write or post comments** — you do. Read-only. Dated artifacts go here as `YYYY-MM-DD.md`.
> **IT —** Cosa produce il digest giornaliero: ogni mattina una lista di post freschi in target su cui vale la pena commentare — ognuno con link + recap + perché + un angolo nella tua voce. **Claude NON scrive né posta i commenti** — li scrivi tu. Solo lettura. Gli artefatti datati vivono qui come `AAAA-MM-GG.md`.

> Risolve il problema #1: *trovare post in target su cui commentare* (`../engagement_playbook.md` §3.5-3.6). Claude dà: **link + recap + perché + angolo** nella tua voce; il commento lo scrivi tu.

## Stato (esempio)

Può girare come task schedulato `{{TASK_NAME_RADAR}}`, **Lun-Ven mattina**. **Apre un browser su LinkedIn** (via Claude in Chrome) e cerca i post — come quando lo fai a mano. **Solo lettura:** non commenta, non posta, non invia.

## Requisiti perché il run automatico funzioni

- L'**app deve essere aperta** all'orario (se è chiusa, parte al successivo avvio).
- **Browser aperto e loggato su LinkedIn**, estensione Claude in Chrome connessa.
- Fai **"Run now"** una volta dal pannello Scheduled per **pre-approvare** i tool del browser (altrimenti il primo run si ferma sui permessi).
- Se LinkedIn chiede login/captcha o il browser non è disponibile, il run **lo dichiara e si ferma** (non inventa post).

## Cosa fa

1. Apre 2-3 **ricerche per argomento** ordinate per "Più recenti" (`../engagement_playbook.md` §3.5 A).
2. Controlla l'**attività recente** di 2-3 poster attivi in target (a rotazione, dalla tua lista di voci/Dream 30 — `../engagement_playbook.md` §5).
3. Seleziona **5-8 post freschi** ad alto segnale e li distilla.

## Output (file `AAAA-MM-GG.md`)

Per ogni post: **Autore (ruolo) + link** · **Recap** · **Perché commentare** · **Angolo per te** (contrarian/dato/domanda nella tua voce — NON un commento finito, mai accondiscendente, mai pitch, mai sminuire la normativa).

## Convenzione di naming

- Un file per giorno: `AAAA-MM-GG.md` (es. `2026-06-19.md`).
- I file sono artefatti datati: si accumulano, non si sovrascrivono.

## A mano

*"esegui il radar"* → lo faccio girare adesso sul browser.

> Nota: X (es. `twitterapi-io`) resta in uso per il **Trend Hunter** (idee di contenuto), non per il radar.

---

> Un esempio compilato e sanitizzato di questa routine (Yempik) vive in `examples/yempik/linkedin/`. I nomi dei poster in rotazione e gli URL di ricerca salvati restano **fuori** dai file condivisi: sono dati di terze parti e preferenze private.
