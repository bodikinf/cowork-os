# Reviews · Recurring operating reviews

> **EN —** Two recurring reviews keep the workspace honest: a **weekly marketing pulse** (data + actions) and a periodic **maintenance review** (knowledge-base hygiene). One dated file per run. Copy the `*.TEMPLATE.md` files to start.
> **IT —** Due review ricorrenti tengono il workspace onesto: una **weekly pulse di marketing** (dati + azioni) e una **maintenance review** periodica (igiene della knowledge base). Un file datato per run. Copia i file `*.TEMPLATE.md` per iniziare.

## Le due cadenze

| Review | Cadenza | A cosa serve | Stampo |
|---|---|---|---|
| **Weekly pulse** | settimanale | Leggere i dati di marketing della settimana, separare fatto/ipotesi/raccomandazione, proporre 3–5 azioni per impatto commerciale. | `weekly_review.TEMPLATE.md` |
| **Maintenance review** | periodica (es. ogni 2 settimane / a fine ciclo) | Verificare che la knowledge base sia aggiornata, coerente e utilizzabile: incoerenze, duplicazioni, informazioni obsolete, indici allineati. | `maintenance_review.TEMPLATE.md` |

## Naming
- `weekly_review_YYYY-MM-DD.md` — un file per pulse (data del run).
- `maintenance_review_YYYY-MM-DD.md` — un file per manutenzione.
- I file datati sono **storia**: non si riscrivono. Le review vecchie possono citare percorsi/file poi cambiati — è normale, restano come riferimento storico.

## Regole valide per entrambe
- **Niente dati inventati.** Se una fonte è offline, dichiaralo e usa l'ultimo dato noto come riferimento.
- **Separa sempre** `[DATO REALE]` / `[IPOTESI]` / `[RACCOMANDAZIONE]`.
- Le modifiche operative (es. all'account pubblicitario) le applica la persona responsabile, non la review.
- Chiudi ogni run con un blocco **Memory Update** (cosa è stato aggiornato, decisioni/domande/rischi/prossime azioni).

## Esecuzione automatica
Entrambe possono girare come **task schedulati** in Cowork (vedi `scheduled-tasks/`). In quel caso il file viene creato dal task; l'umano legge e agisce.
