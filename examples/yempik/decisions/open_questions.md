> **EN —** Filled example (sanitized): Yempik's open questions. Question structure kept; tool/team IDs, lead/competitor names, amounts → `[illustrativo]` / generic.
> **IT —** Esempio compilato (sanitizzato): domande aperte di Yempik. Struttura mantenuta; ID strumenti/team, nomi lead/competitor, importi → `[illustrativo]` / generici.

---

# Yempik — Domande aperte & ipotesi da validare

> Cose non ancora decise, non chiare, o assunte. Le decisioni prese stanno in `decisions_log.md`.
> 🔴 bloccante · 🟠 importante · 🟡 da chiarire · 🟢 opportunità · ✅ risolto · ~~barrato~~ superato.

## Setup tecnico (bloccanti operativi)
- 🔴 **Pipeline dati di reporting offline (free trial scaduto).** Ogni query (Google Ads, GA4, Keyword Planner, Trends) restituisce errore "trial expired": i metadati restano leggibili, ma **nessun dato di performance** è estraibile. Lo stato delle sorgenti risulta `AUTHENTICATED` (OAuth valido) → il gate **non è il token ma l'abbonamento di team**: riautenticare non sblocca nulla. **Da decidere:** sottoscrivere un piano **oppure** adottare un feed manuale settimanale (~6 numeri Ads + 3 GA4 incollati a mano). *Nuova, `[illustrativo]`.*
  - ✅ **Aggiornamento successivo: campagne FERMATE.** La spesa paid si è interrotta → **l'urgenza "si spende al buio" decade**. Il blocco resta utile solo per l'**analisi retrospettiva**, non più come rischio di spesa in corso.
- **Account Google Ads:** esiste un account già usato per un altro sito (diverso da yempik.com). **Da decidere:** creare un nuovo account dedicato a Yempik o riusare quello esistente, e come impostare di conseguenza le conversioni. *Discusso, decisione non ancora registrata.*
- ~~**Tracciamento conversioni installato e testato?**~~ **RISOLTO:** meccanismo verificato nel codice (tag + thank-you page + email) e confermato funzionante. Registrate le **prime conversioni reali** → il tubo conversione scatta correttamente in produzione.
- **Consent Mode v2 + CMP + GA4/Tag Manager** effettivamente attivi? — da verificare.

## CRM / gestione lead
- 🟠 **Manca una tabella/lista dedicata ai lead inbound del sito.** Oggi l'unica base è la pipeline di un prodotto verticale, un contesto diverso. **Da decidere:** creare una tabella "Lead inbound" o una view/tag separati. Più urgente ora che arrivano più lead a settimana.
- ~~**Dove vive il registro opportunità/pipeline nel workspace?**~~ **RISOLTO per struttura.** Il registro vive ora in **`business-development/`**: tabella lead nel README, partnership/canale in un file dedicato, una cartella per lead.
- **Connettore email dà "precondition failed"** sulla creazione bozze — da verificare l'account collegato / ri-autorizzazione, così le risposte ai lead possono essere preparate in automatico.

## Contenuti / prova
- 🟡 **Quali clienti possono essere citati con nome** e con quale **numero di risultato** per i case study? La homepage già **nomina** clienti e una **testimonianza** marcata bozza → confermare formalmente quali sono **pubblicabili** (una citazione "in bozza" renderizzata live è un rischio legale/di fiducia).
- 🟡 **Coerenza entità "Made in Italy" ↔ entità legale:** il sito si presenta come "software house italiana / Made in Italy" ma l'entità legale è altrove. **Da decidere** la formulazione (coerenza per answer engine + attrito fatturazione verso PMI italiane) e come gestire la fatturazione verso clienti italiani. *Nuova, `[illustrativo]`.*
- **Prezzi 3.500 € / 8.000 €:** confermati come definitivi o indicativi da rivedere? *(Già pubblicati come "da" su `/prezzi`, homepage, money page, FAQ e `llms.txt`.)*

## Strategia (scelte non ancora prese)
- 🟢 **Funnel B2C "Formazione/Corsi AI"** (cluster ad alto volume con intento d'acquisto): attivarlo, anche solo come lead magnet? *Ipotesi, non decisa.*
- 🟢 **Canale partner — termini economici da decidere.** Sconto white-label sul listino e fee referral: valori di partenza nella bozza di accordo, **non confermati**.
- 🟢 **Canale partner — anti-poaching reciproco o solo a carico Yempik?** La clausola "non contattiamo i tuoi clienti" è la leva di fiducia; da decidere se renderla reciproca.
- 🟢 **Demand generation su LinkedIn/Meta** per creare volume oltre la Search? *Ipotesi, non decisa.*
- **Re-weighting del budget** verso agenti/automazione tenendo "Software house" secondario: *ipotesi operativa proposta*, **da confermare/superare con i primi dati** (i dati di conversione indicano l'opposto — vedi `marketing/campaigns.md`).
- **Variante landing dedicata `/automazioni-ai`** per il gruppo Automazione: da valutare.

## Ipotesi esplicite da validare con dati reali
- **Valore medio cliente = `[illustrativo]`** (usato nel simulatore): è una stima, non un dato storico.
- **Tassi del simulatore** (conv. landing, lead→SQL, chiusura): ipotesi da calibrare dopo le prime settimane.
- **Lettura competitiva:** basata sull'analisi di un solo concorrente + Keyword Planner; da rivedere con più concorrenti.

## Da completare / domande per il fondatore
- ~~Anno di fondazione~~ **RISOLTO** *(`[illustrativo]`)*: dato verificato a registro; il `foundingDate` pubblicato live (schema + llms.txt) era **errato** e corretto. → L'esperienza del *fondatore* come builder (~anni) è cosa distinta dalla data di costituzione della società.
- **Made in Italy ↔ sede legale:** la sede legale registrata e la presentazione pubblica "software house italiana" vanno rese coerenti (già aperto sotto "Contenuti / prova").
- Boilerplate/payoff ufficiale e linee guida brand (logo, colori) per `context/tone_of_voice.md`.

## Formazione AI B2B (linea in valutazione)
Decisioni aperte:
- **Modello di prezzo:** abbandonare il €/h per un prezzo **a pacchetto/giornata sul valore**? *(Raccomandato. Da confermare.)*
- **Scala prodotti a livelli** (Briefing breve / Adoption Sprint medio / Lab esteso): adottarla? *Proposta, non confermata.*
- **Accreditamento fondi interprofessionali** per togliere l'obiezione prezzo: serve ente accreditato o partnership? **Rotta proposta: partner con ente accreditato** (gestisce pratica/rendicontazione, Yempik mette corso + docente).
- **Aggiungere linea "Formazione AI" al sito** e collegarla al cluster "Formazione/Corsi AI" (già mappato come opportunità non attivata)?
> **Allineamento fondatore:** target reale = **responsabili di ufficio/funzione**, non C-level → formato medio confermato. Angolo normativo declassato da gancio principale a contesto. Posizionamento = imprenditore che usa e sviluppa AI da anni. Prima mossa: **edizione pilota** dalla rete a prezzo amico per costruire prova/testimonial.

## Stack didattico corso + rischi
- **Obiettivo corso:** ogni partecipante esce con UN processo scelto, standardizzato, un primo **prototipo funzionante** e il percorso verso la produzione (NON un'automazione in produzione in poche ore).
- **RISCHIO:** costruire il corso attorno a un singolo vendor (research preview) = dipendenza da roadmap/disponibilità + possibile attrito con clienti che usano altri stack. **Mitigazione:** metodo agnostico, lo strumento è il mezzo, fallback su altri assistenti.
- **Domanda aperta:** come accedono i partecipanti allo strumento in aula (piano proprio / seat del cliente / sandbox)? Automatizzare processi VERI richiede dati/strumenti reali → tocca IT/sicurezza → favorisce l'**in-house**; per aule aperte usare dati di esempio/sandbox.

## Prodotti verticali — domande di portata Yempik
- 🟡 **Possibile collisione di naming** tra un prodotto Yempik e un prodotto concorrente: impatto su posizionamento/marchio/SERP da valutare.
- **Listino del prodotto verticale** *(`[illustrativo]`/mese)*: confermare come prezzo ufficiale a regime e relativa unità di misura.
- **Narrativa servizi vs prodotti verticali:** quanto i prodotti propri devono comparire nei servizi su commessa vs restare verticali a sé (già aperta in `context/services.md`).

## Open-source `cowork-os` (da decidere prima del push)
- **Nome definitivo del repo.** Nome di lavoro `cowork-os`; alternative valutate (generico / brandizzato / SEO).
- **Dove ospitarlo:** account GitHub personale del fondatore vs organizzazione Yempik — impatta credito e posizionamento.
- **Cosa mostrare negli esempi "Yempik":** tenere i prezzi pubblici 3.500/8.000 € (già pubblici sul sito) — *attualmente tenuti*; mostrare i nomi dei prodotti propri o tenerli generici — *attualmente generici*. Da confermare.
- **Re-verifica umana dell'anonimizzazione prima del push.** La sweep automatica è pulita; una rilettura umana è consigliata prima di rendere pubblico.

> **Nota di metodo:** questo file è anche dove finiscono le note "esplorative" su nuovi prodotti/offerte prima che diventino workstream. Quando un'esplorazione diventa reale, promuovila a `products/<nome>/` o `business-development/` e logga la decisione. Tieni **fuori** da un file pubblico: nomi di lead/clienti reali, importi reali, accessi/credenziali, dettagli di deliverable di clienti.
