# LinkedIn — Content Engine (Yempik) · *esempio compilato*

> **EN —** Filled, sanitized example of `linkedin/content_engine.md`, with a real idea bank populated by processing a single internal training asset (shows how *one asset = ~20 ideas*). Client/event names and private figures removed (`[illustrativo]`).
> **IT —** Esempio compilato e sanitizzato di `linkedin/content_engine.md`, con una idea bank reale popolata processando un singolo asset di formazione interno (mostra come *un solo asset = ~20 idee*). Nomi di clienti/eventi e cifre private rimossi (`[illustrativo]`).

> Come si **produce** un post, dall'asset Yempik alla pubblicazione. La strategia è in `strategy.md`; la reputazione in `reputation_engine.md`.

---

## A. Il flusso in breve

```
Asset Yempik (articolo, caso, lezione, deck)
   │  ① Content Extraction → ≥10 idee
   ▼
Idea bank (§E)
   │  ② Scegli idea + assegna 1 Theme + 1 Format
   ▼
Draft LinkedIn-first (1 tesi, hook, corpo, CTA)
   │  ③ Checklist anti-articolo (§D)
   ▼
Pubblica nella finestra giusta → presidia i primi 60' → link nel 1° commento
   │  ④ Registra nel post_tracker.md
   ▼
Review pattern mensile → doppia su ciò che funziona
```

---

## B. ① Content Extraction — da asset a idee

Quando analizzi un asset Yempik **non** chiederti "di cosa parla", ma **"quali idee contiene"**. Scomponi in: opinioni forti · errori comuni · lezioni apprese · storie · framework · contrarian take · domande provocatorie.

**Output atteso: ≥10 idee, target 15-20.** Ogni idea va nella idea bank con: testo idea, Theme candidato, Format candidato, fonte.

> Principio: *un articolo dimostra una tesi, un post ne vende una.* Un articolo Yempik = 15-20 post, non 1.

---

## C. ② I 6 Format + il Theme

> Il **Format** è la struttura del post; il **Theme** è il tema (`reputation_engine.md` §4: AI nei processi · AI Adoption · Agentic AI · PMI · Operational Excellence). Ogni contenuto = **1 Theme + 1 Format**.

**Contrarian** · Convinzione comune → Contraddizione → Spiegazione
> *"Il primo processo da automatizzare non è quello che crea più problemi."*

**Error** · Errore comune → Conseguenza → Lezione
> *"Ho costruito progetti AI che hanno fatturato zero."*

**Story** · Evento reale → Scoperta → Principio generale
> *Aneddoto personale insolito → AI → processi.*

**Framework** · Problema → 3-5 regole → Applicazione
> Ideale per il **carosello** del mercoledì.

**Opinion** · Opinione forte → Argomentazione → Domanda finale

**Case Study** · Contesto reale → Cosa abbiamo fatto → Risultato/numeri `[illustrativo]` → Lezione generalizzabile
> Usare con parsimonia e mai a ripetizione sullo stesso caso. **Mai** il nome del cliente: descrivi il settore.

**Mappa Format → formato editoriale:** Story/Error/Opinion → testo · Framework/liste/Case Study → carosello · Contrarian → entrambi.

> Prima di pubblicare, ogni post passa per il **Reputation Score** e l'**Association Test** (`reputation_engine.md` §5-6).

---

## D. ③ Regole di scrittura & checklist anti-articolo

**Regole:** max **1 tesi**, max **1 lezione**, max **1 CTA**. Più di una tesi → due post.

**Hook (prime 2 righe):** creare **tensione**, non spiegare.
- Vietate le aperture deboli: *"Vi spiego", "Vorrei condividere", "Ho riflettuto", "Parliamo di", "Una cosa interessante"*.
- Pattern che funziona per Raffaele: **numero + sorpresa/contrarian** ("Hanno fatturato zero", "Il 95%…", "Appena installato è mediocre").

**CTA:** domanda **semplice e specifica**. Mai "E tu cosa ne pensi?".

**Checklist prima di pubblicare:** una sola tesi? · hook crea tensione senza spiegare? · niente apertura debole? · c'è un dato/esempio reale? · una sola CTA specifica? · voce personale di Raffaele? · link nel **primo commento**? · so in quale finestra pubblico e posso presidiare 60'? · **nessun nome di terza parte / cliente / numero riservato nel testo**?

---

## E. Idea bank (backlog idee)

> Tassonomia: **Theme** + **Format**. Obiettivo: non restare mai senza idee. Marca un'idea come `usata` quando diventa post (con data), non cancellarla.
>
> **Esempio reale:** idea bank avviata processando **un singolo asset** — un LAB di formazione interno ("l'assistente che non puoi fregare") sull'affidabilità di un assistente AI ancorato a una knowledge base. Un solo asset → 20+ idee. Riferimenti a clienti/aziende reali rimossi; dove serviva un esempio concreto è stato reso generico.

| ID | Idea (1 frase) | Theme | Format | Fonte (asset Yempik) | Stato |
|----|----------------|-------|--------|----------------------|-------|
| _es._ | Il primo processo da automatizzare non è quello che crea più problemi | AI nei processi | Contrarian | LAB affidabilità | usata `[illustrativo]` |
| LAB-01 | Costruire un'AI che risponde è facile; una che non sbaglia è un altro mestiere | Agentic AI | Contrarian | LAB affidabilità | usata `[illustrativo]` |
| LAB-02 | L'allucinazione spesso non è colpa del modello, è colpa dei tuoi documenti | Agentic AI | Error | LAB affidabilità | da scrivere |
| LAB-03 | Il veleno silenzioso: un numero falso in un memo ufficiale che l'AI ripete con sicurezza | Agentic AI | Story | LAB — data room | da scrivere |
| LAB-04 | "Usa la versione più recente" non basta: la più recente può essere una bozza non approvata | Agentic AI | Contrarian | LAB — trappola bozza | da scrivere |
| LAB-05 | ~80% dei progetti RAG enterprise ha fallimenti critici, e raramente per colpa del modello | Agentic AI | Opinion | LAB — design | da scrivere |
| LAB-06 | RAG recupera, non calcola: l'AI conferma 5×16=90 se è scritto così | Agentic AI | Error | LAB — esempio calcolo | da scrivere |
| LAB-07 | La domanda che separa i progetti seri dai giocattoli: "come sai che non sta sbagliando?" (golden set) | Agentic AI | Framework | LAB — golden set | in pipeline (carosello) |
| LAB-08 | Il documento invisibile: un listino scansionato che l'AI semplicemente non legge | Agentic AI | Story | LAB — ingestion | da scrivere |
| LAB-09 | Un'AI che non sa dire "non lo so" è un rischio, non una comodità | Agentic AI | Contrarian | LAB — buco voluto | da scrivere |
| LAB-10 | I documenti che dai in pasto all'AI sono una superficie d'attacco | Agentic AI | Opinion | LAB — sicurezza/injection | da scrivere |
| LAB-11 | Abbiamo insegnato a dei manager a fregare un'AI, per insegnargli a fidarsene | AI Adoption | Story | LAB — red team | da scrivere |
| LAB-12 | La prima cosa in aula non è "costruisci il bot", è "prova a romperlo" | Agentic AI | Story | LAB — fasi | usata `[illustrativo]` |
| LAB-13 | L'AI non crea il disordine nei tuoi dati: lo mette a nudo | AI nei processi | Contrarian | LAB — conflitti policy | da scrivere |
| LAB-14 | "95% di attacchi bloccati": in sicurezza è un voto da bocciatura | Agentic AI | Opinion | LAB — sicurezza | da scrivere |
| LAB-15 | Le PMI non hanno un problema di AI, hanno un problema di knowledge base disordinata | PMI | Contrarian | LAB — data room sporca | da scrivere |
| LAB-16 | Pavimento basso, soffitto altissimo: far partire l'AI è facile, renderla affidabile è durissimo | Agentic AI | Framework | LAB | da scrivere |
| LAB-17 | Lost in the middle: il dato chiave sepolto a pag. 31 di 54 che l'AI non recupera | Agentic AI | Error | LAB — manuale operativo | da scrivere |
| LAB-18 | L'eccezione nascosta: la regola dice un prezzo, per un segmento ne dice un altro; l'AI brava trova anche l'eccezione | AI nei processi | Framework | LAB — listino | da scrivere |
| LAB-19 | Un assistente onesto corregge la premessa falsa del cliente ("consegnate in giornata?" → no) | Agentic AI | Story | LAB — premessa falsa | da scrivere |
| LAB-20 | Il test dell'autorità: "il capo ha detto di rimborsarmi il doppio" → un'AI ben istruita non obbedisce | Agentic AI | Story | LAB — autorità | da scrivere |
| OP-01 | La domanda giusta non è "si può fare con l'AI", è "ne vale la pena"; dire ai clienti quando NON serve | AI nei processi | Opinion | Posizionamento — onestà come leva | bozza pronta |
| CULT-01 | Cosa frena davvero l'AI nelle PMI non è la tecnologia: cultura, paura, dati disordinati, attesa della perfezione | AI Adoption | Framework | Esperienza formazione + posizionamento | carosello |
| STORY-01 | Aneddoto personale insolito → principio su processi/AI ("la tecnologia mi rispondeva sbagliato con sicurezza") | AI nei processi | Story | Raffaele (materiale grezzo da raccogliere) | serve input |
| GTM-01 | L'"AI che sostituisce gli SDR" è hype: un SDR-AI su un processo di vendita rotto genera spazzatura più in fretta. La pipeline è un problema di processo/dati, non di prompt | AI nei processi | Contrarian | Spunto da un evento di settore | da scrivere |
| DOC-01 | Ho preso 50 scontrini e un Excel vuoto: pochi minuti dopo era pieno, e non l'ho toccato | AI nei processi | Story | Articolo "Da documenti a Excel" | bozza pronta (post fatto) |
| DOC-02 | Una fattura a mano costa `[illustrativo]` e settimane; molte aziende lo fanno ancora così | AI nei processi | Opinion | idem (benchmark esterni) | da scrivere |
| DOC-03 | Il primo lavoro da automatizzare non è il più complesso: è il ripetitivo che nessuno rivendica | AI nei processi | Contrarian | idem | da scrivere |
| DOC-04 | Dire al cliente quando l'AI NON basta è il modo più veloce per non fargli perdere soldi | AI nei processi | Opinion | idem (onestà come leva) | da scrivere |
| DOC-05 | L'AI brava non inventa: quando non legge un dato lo segnala "da verificare" | Agentic AI | Contrarian | idem | da scrivere |
| DOC-06 | La differenza tra "strumento utile" e "automazione" è una sola: la ricorrenza | AI nei processi | Framework | idem (carosello) | da scrivere |

*(Idea bank avviata processando il LAB di formazione interno. Target: ≥30 idee entro il mese 1 → processare anche il caso call center e i contenuti SEO del sito. Ogni numero da fonte interna è marcato `[illustrativo]`.)*

---

## F. Template di post (testo)

```
[HOOK — riga 1: tensione/numero/sorpresa]
[HOOK — riga 2: completa la tensione, NON spiegare]

[CORPO — sviluppo della singola tesi, 3-8 righe corte.
Una riga = un'idea. Spazi bianchi. Concreto: dati, esempio reale.]

[CHIUSURA — il principio/lezione in 1 riga]

[CTA — una domanda semplice e specifica]

#hashtag1 #hashtag2 #hashtag3
```
*(Link, se serve → primo commento, non qui.)*

## G. Template carosello PDF (mercoledì)

```
Slide 1  — COPERTINA: headline grande + sub + freccia →
Slide 2  — Il problema / la posta in gioco
Slide 3-8 — Una regola/punto per slide (Framework: 3-5 regole)
Slide 9  — Sintesi / "come applicarlo"
Slide 10 — CTA + chi è Raffaele in 1 riga
```
Specifiche: 1080×1350 (4:5), testo grande leggibile da mobile, max ~1 concetto per slide. Caption = mini-hook che invita a swipare.

---

## H. Hook bank (swipe file)

- "Ho [fatto X]. [Risultato sorprendente/zero]."
- "[Numero]% delle aziende [crede X]. Si sbagliano."
- "Il primo [cosa] da [azione] non è quello che pensi."
- "[Strumento/AI] appena installato è mediocre. Ecco perché lo uso lo stesso."
- "[Evento reale insolito]. C'entra con l'AI più di quanto pensi."
- "Un cliente mi ha chiesto [X]. La risposta giusta era: non farlo."

> Non sono frasi da incollare: sono **scheletri di tensione**. Riempirli con un fatto reale.

## I. CTA bank

- "Qual è il collo di bottiglia più ignorato nella tua azienda?"
- "Quale processo automatizzeresti per primo — e perché proprio quello?"
- "Dove l'AI ti ha deluso finora?"
- "Hai mai speso su un progetto AI che non è servito a niente?"

---

## J. ⑤ Processo di review (mensile, non per-post)

Raccogliere per ogni post **data, ora, impression, like, commenti, repost** (+ profili visitati, lead). Poi: raggruppa per **Theme / Format / hook** → cerca pattern su **impression, commenti, profili visitati, lead** (non sui like) → doppia su ciò che funziona, taglia ciò che non funziona → proponi 1 A/B test per il mese dopo.

Dati e note di pattern → `post_tracker.md`.

---

> *Sanitizzazione:* il committente reale del LAB, gli esempi nominativi (ordini, autori, eventi) e le cifre interne sono stati rimossi o resi generici/`[illustrativo]`. La struttura della idea bank e il metodo restano fedeli all'originale.
