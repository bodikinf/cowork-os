# Monitoraggio campagne · Ad-monitoring reports

> **EN —** Dated campaign-monitoring snapshots. One file per report, named `monitoraggio_adv_YYYY-MM-DD.md`. These are point-in-time data pulls — the strategy lives in `../strategy.md`, the structure in `../campaigns.md`.
> **IT —** Snapshot datati di monitoraggio campagna. Un file per report, nominato `monitoraggio_adv_YYYY-MM-DD.md`. Sono fotografie di un momento — la strategia sta in `../strategy.md`, la struttura in `../campaigns.md`.

## Convenzione di naming
- `monitoraggio_adv_YYYY-MM-DD.md` — la data è quella del report (giorno in cui i dati sono stati estratti).
- Un file per data. **Non** riscrivere un report vecchio: i report sono storia. Se i dati cambiano, scrivine uno nuovo.
- Evita nomi ambigui legati al "giorno N di campagna" (es. `check_dayN`): usa sempre la data assoluta.

## Cosa mettere in un report
- Periodo coperto e fonte dati (con nota se la fonte era offline/parziale).
- Metriche principali per gruppo/canale: impression, click, spesa, conversioni, CPA, impression share persa.
- 1–2 insight e le azioni proposte (le modifiche all'account le applica chi gestisce il paid).
- Separa sempre **fatto** (`[DATO REALE]`), **ipotesi** (`[IPOTESI]`) e **raccomandazione** (`[RACCOMANDAZIONE]`).

## Privacy
In un repo pubblico tieni i numeri reali **fuori** (vedi `.gitignore`): sostituiscili con `[illustrativo]`, oppure mantieni questi report in una copia privata del workspace.
