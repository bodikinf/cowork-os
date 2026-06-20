# LinkedIn — Editor Workflow (il tuo editor personale)

> **EN —** The runnable "personal editor": a fixed 8-step workflow that turns any source asset into a ready-to-publish post (20 ideas → classify → top 5 → 3 hooks each → Reputation Score + Association Test → today's post → update the system). Invoke with *"esegui l'editor su [asset]"*. Update when the steps or scoring change.
> **IT —** L'"editor personale" runnable: un workflow fisso a 8 step che trasforma qualsiasi asset in un post pronto da pubblicare (20 idee → classifica → top 5 → 3 hook → Reputation Score + Association Test → post di oggi → aggiorna il sistema). Si invoca con *"esegui l'editor su [asset]"*. Aggiornare quando cambiano gli step o lo scoring.

> **Cos'è:** un workflow **obbligatorio e ripetibile**. Quando `{{FOUNDER}}` dice *"esegui l'editor su [articolo/asset]"*, Claude segue **esattamente** questi step, in ordine, senza saltarne nessuno.
>
> **Differenza da `content_engine.md`:** quello è il *riferimento* (regole, banche, template). Questo è la *procedura runnable* che li applica. Le regole di scrittura e i 6 Format vivono lì; qui si esegue.
>
> **Non è una vanity machine:** si ottimizza per impression, **commenti, profili visitati, lead** — mai per like.

---

## Input

Un asset `{{COMPANY}}`: articolo del sito, caso reale, deck, bozza, post pubblicato, o trascrizione. Se manca, Claude lo chiede prima di iniziare.

## Output finale (cosa consegna sempre)

1. 20 idee classificate (tabella).
2. Le 5 idee più forti con motivazione.
3. 3 hook per ciascuna delle 5 (15 hook).
4. Punteggio **euristico** Reach + Lead per le 5.
5. **1 post pronto da pubblicare oggi**, completo (hook A + variante B, corpo, CTA, hashtag, link nel 1° commento), coerente col formato/Theme che il calendario assegna a oggi.
6. Aggiornamento del sistema: idea bank, calendario, riga nel tracker.

---

## STEP 0 — Context check (obbligatorio)

Prima di leggere, Claude stabilisce:
- **Che giorno è e cosa tocca oggi** (da `calendar.md`): Lun → testo · Mer → carosello · Ven → testo. Questo vincola lo Step 7.
- **Theme plausibili** dell'asset (i tuoi pillar — `reputation_engine.md` §4).
- **Bilanciamento corrente** dei Theme nel mese (da `post_tracker.md` / `calendar.md`): se un Theme è sotto-rappresentato, ha priorità a parità di forza.

## STEP 1 — Leggi l'asset

Lettura per **estrazione**, non per riassunto. Domanda guida: *"Quali idee contiene?"*, non *"di cosa parla?"*.

## STEP 2 — Estrai 20 idee

Forcing function: **20 idee** (minimo accettabile 15). Ogni idea = una frase autoconclusiva che potrebbe reggere un post da sola. Pescare da: opinioni forti, errori comuni, lezioni apprese, storie, framework, contrarian take, domande provocatorie.

## STEP 3 — Classifica (Theme + Format)

Per ogni idea assegna **1 Theme + 1 Format** (vedi `reputation_engine.md` §4):
- **Theme:** i tuoi pillar (`{{PILLAR_1}}` · `{{PILLAR_2}}` · `{{PILLAR_3}}` · `{{PILLAR_4}}`)
- **Format:** Story · Contrarian · Framework · Opinion · Error · Case Study

| # | Idea (1 frase) | Theme | Format |
|---|----------------|-------|--------|
| 1 | | | |
| … | | | |
| 20 | | | |

## STEP 4 — Seleziona le 5 più forti

Criteri di selezione (in ordine):
1. **Tensione**: si può aprire con un hook che ferma lo scroll?
2. **Concretezza**: c'è un dato/esempio/numero reale (non genericità da `{{CATEGORY}}`)?
3. **Rilevanza ICP**: tocca un pain vero di `{{ICP}}`?
4. **Aggancio commerciale**: porta naturalmente verso un motore `{{COMPANY}}` (`{{SERVICE_1}}`/`{{SERVICE_2}}`/…)?
5. **Bilanciamento Theme** (da Step 0): a parità, vince il Theme sotto-rappresentato.

Output: le 5 idee con 1 riga di motivazione ciascuna.

## STEP 5 — 3 hook per idea (15 hook)

Per ciascuna delle 5, scrivi **3 varianti di hook** (prime 2 righe). Regole:
- Creano **tensione**, non spiegano.
- Almeno una variante usa il pattern **numero + sorpresa/contrarian** (es. "Ho fatto X. Risultato: zero.").
- **Vietate** le aperture deboli: "Vi spiego", "Vorrei condividere", "Ho riflettuto", "Parliamo di", "Una cosa interessante" → se compaiono, scarta e riscrivi.
- Voce personale di `{{FOUNDER}}` (`../context/`), non tono da brand.

## STEP 6 — Reputation Score + Association Test (primario) · Reach/Lead (secondario)

> Si ottimizza la **reputazione**, non l'engagement (`reputation_engine.md`). Il Reputation Score è il driver primario; la Reach/Lead è un segnale di distribuzione secondario.

**A) Reputation Score** — per ciascuna delle 5 idee, valuta 1-10:
- **Utilità** · **Originalità** · **Posizionamento** (rafforza `{{CATEGORY}}` → `{{FOUNDER}}`) · **Conversazione**

`Reputation Score = (Originalità + Posizionamento) × 2 + Utilità + Conversazione` (range 6-60). Soglie: ≥44 forte · 32-43 ok · <32 rivedere.

**B) Association Test (gate)** — "Questo contenuto aumenta la probabilità che si associ `{{CATEGORY}}` a `{{FOUNDER}}`?" Se **NO** → ripensa, anche se il Reputation Score è alto.

**C) Reach/Lead (secondario, 1-5)** — solo come segnale di distribuzione:
- *Reach:* forza hook · carica contrarian/emotiva · fit formato · condivisibilità.
- *Lead:* pain di business? · CTA verso un motore `{{COMPANY}}`? · parla al decisore `{{ICP}}`?

Resa: `Reputation: 46/60 · Association: ✅ · Reach ●●●○○ (3.2) · Lead ●●●●○ (4.0)`.

> ⚠️ Anti-trappola: Reach alta ma Reputation/Lead bassi = post "da like", non da reputazione → segnalalo.

## STEP 7 — Il post di OGGI

1. Tra le 5, scegli quella che **passa l'Association Test**, ha il **Reputation Score più alto** e **incastra il formato di oggi** (Step 0); a parità, guarda il Lead. Se nessuna calza il formato di oggi, dillo e proponi la più vicina (o suggerisci di spostare il formato).
2. Scrivi il **post completo e pubblicabile**:
   - Hook scelto (**A**) **+ una variante B per A/B test**.
   - Corpo: 1 sola tesi, righe corte, un dato/esempio reale, spazi bianchi.
   - 1 CTA = domanda semplice e specifica.
   - 3 hashtag.
   - Eventuale link → indicato per il **primo commento**, non nel corpo.
   - Se oggi è Mer (carosello): struttura le 10 slide (`content_engine.md` §G) invece del testo lungo.
3. Passa la **checklist anti-articolo** (`content_engine.md` §D) e dichiarala superata.
4. Indica la **finestra di pubblicazione** consigliata e ricorda di presidiare i primi 60'.

## STEP 8 — Aggiorna il sistema (loop di chiusura)

Obbligatorio, non opzionale:
- **Idea bank** (`content_engine.md` §E): aggiungi le 20 idee (o almeno le 15 migliori) con stato; marca come `usata + data` quella diventata post.
- **Calendario** (`calendar.md`): inserisci il post di oggi nella riga del giorno.
- **Tracker** (`post_tracker.md`): crea la riga del post (data, ora, Theme, Format, tipo ed., hook) pronta per i dati a 48-72h.
- **Ri-calibrazione**: se ci sono già dati nel tracker, confronta l'euristica Step 6 con la reach/commenti reali dei post simili e annota lo scostamento (così l'euristica migliora).

---

## Regola d'oro

Se in qualsiasi step emerge **più di una tesi** in un singolo post → si divide in due post. Un post vende **una** tesi.

## Come invocarlo

> "Esegui l'editor su [link/asset]" · "Editor: dammi il post di oggi da [asset]" · "Fai girare il workflow editor su [bozza]".

> *Nota:* l'editor esiste anche come **Skill `.skill` installabile** (invocabile ovunque con lo slash). La differenza: la Skill è autonoma → consegna blocchi "da incollare" invece di scrivere direttamente su idea bank/calendario/tracker. Questo file-workflow, dentro il Project, chiude il loop scrivendo sui file.
