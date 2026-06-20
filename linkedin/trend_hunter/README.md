# LinkedIn — Trend Hunter (routine automatizzata)

> **EN —** What the automated weekly trend-hunter routine produces: dated reports of AI/industry signals, reinterpreted through your Category Thesis, that feed the idea bank. Human selection stays in the loop. Dated artifacts go in this folder as `YYYY-MM-DD.md`.
> **IT —** Cosa produce la routine automatizzata settimanale: report datati di segnali di settore, reinterpretati via Category Thesis, che alimentano la idea bank. La selezione finale resta umana. Gli artefatti datati vivono in questa cartella come `AAAA-MM-GG.md`.

> Routine che alimenta il Reputation Engine (`../reputation_engine.md` §8). Usa i trend come **input**, reinterpretati via Category Thesis — non li insegue. La selezione finale resta **umana**.
>
> **Stato (esempio):** può girare come task schedulato `{{TASK_NAME_TREND}}`, **2×/sett: lunedì (completo) + giovedì (pulse)**, web/RSS + X.

## Cosa fa

- **Lunedì (run completo):** raccoglie i segnali della settimana (web/RSS + X), monitora le ~10 voci chiave (People Map, `../reputation_engine.md` §7), fa comment mining sulle discussioni più calde, filtra tutto via Category Thesis e produce il report con idee post.
- **Giovedì (pulse leggero):** scansione veloce trend X + web → 3 idee fresche per alimentare il post di venerdì.

## Fonti

- **Web search** mirata sui tuoi temi (`{{PILLAR_1}}` · `{{PILLAR_2}}` · novità di settore, strumenti).
- **RSS / newsletter** di settore (es. testate e blog tecnici/di ricerca pubblici che segui).
- **X** via MCP (es. `twitterapi-io`): trend (mondiale + locale), ricerca sui Theme, ultimi post delle voci della People Map, reply (comment mining).

## Budget

Le API a consumo hanno un costo per lettura. Imposta un **tetto per run** (es. ~400 letture/run il lunedì, ~150 il giovedì) e un **budget mensile** (es. `{{AMOUNT}}`/mese) con margine. La chiave vive nella config dell'MCP, **non in chat**.

## Output (file `AAAA-MM-GG.md` in questa cartella)

1. **Trend emergenti** (con fonte/link).
2. **Trend saturi** — da evitare o ribaltare.
3. **Opportunità poco presidiate**.
4. **Idee post per `{{FOUNDER}}`** — ognuna con **Theme + Format** + hook abbozzato.
5. **Proposte per la idea bank** — 2-3 righe da approvare (non inserite in automatico).
6. *(solo lunedì)* **Proposte People Map** + insight **Comment Mining** (linguaggio reale del mercato).

## Convenzione di naming

- Un file per run, datato: `AAAA-MM-GG.md` (es. `2026-06-22.md`).
- Il run completo (lunedì) e il pulse (giovedì) possono coesistere nello stesso file settimanale o in due file distinti — scegli una convenzione e tienila.

## Eseguirlo a mano

Di' a Claude *"esegui il trend hunt"* → fa girare la routine adesso, senza aspettare lunedì/giovedì.

---

> Un esempio compilato e sanitizzato di questa routine (Yempik) vive in `examples/yempik/linkedin/`. Le voci pubbliche monitorate (People Map) restano **fuori** dai file condivisi.
