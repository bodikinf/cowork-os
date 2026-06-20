# Mission Log — Evidence Log (vendor AI) · *esempio compilato*

> **EN —** Filled, sanitized example of `missions/_TEMPLATE/mission_log.md`. Every real name, company number, address, client list, program amount and private URL is removed; dates are `[illustrativo]`.
> **IT —** Esempio compilato e sanitizzato di `missions/_TEMPLATE/mission_log.md`. Ogni nome reale, numero societario, indirizzo, elenco clienti, importo di programma e URL privato è rimosso; le date sono `[illustrativo]`.

> Ogni azione importante documentata, per evitare loop e capire cosa è già stato tentato.

```yaml
- date: "[illustrativo]"
  route: 1-2-3-4 (intelligence)
  action: Prima passata di intelligence (web research) su canali ufficiali, persone (ruoli), partner ecosistema del vendor.
  target: vendor AI (canali ufficiali, EMEA/Italia, ecosistema)
  status: done
  result: >
    Trovati e verificati: partner network ufficiale (con candidatura aperta e partner hub);
    percorso di certificazione; programma per startup (crediti + accesso eventi);
    SEDE ITALIANA aperta di recente, guidata da un referente per il Sud Europa (ruolo, non nome);
    aziende italiane già clienti del vendor [elenco rimosso]; un partner locale; un ruolo dedicato a startup/eventi; precedente workshop locale.
  next_step: Pubblicare 1 proof of work; preparare outreach alla sede locale (Route 1) appoggiato al proof of work.
  notes: Nessun contatto inviato. Contatti diretti non ancora reperiti.

- date: "[illustrativo]"
  route: setup
  action: Creata struttura della missione + cartella workflow con tutti i file iniziali.
  target: repo locale yempik
  status: done
  result: mission.md, route_map.md, next_actions.md, mission_log.md, + asset di supporto (canali ufficiali, mappe per ruolo, proof of work, outreach)
  next_step: Vedi next_actions.md
  notes: Gli asset di outreach sono BOZZE non approvate.

- date: "[illustrativo]"
  route: fact-check / fix
  action: Verifica entità societaria e correzione dei dati di fondazione errati sul sito.
  target: Yempik
  status: done
  result: >
    Confermata la forma societaria e la data di costituzione reale; corretto il foundingDate sul sito
    (structured data + llms.txt) e in memoria. Implicazione: Yempik ELEGGIBILE al programma startup del vendor.
  next_step: deploy del sito; applicare al programma startup.
  notes: I dettagli societari reali (ragione sociale, numero registro, sede) sono OMESSI da questo esempio.

- date: "[illustrativo]"
  route: 1 (sede locale / persone)
  action: Inviate 2 richieste di collegamento LinkedIn con nota (autorizzazione esplicita di Raffaele).
  target: referente sede locale + responsabile internazionale startup (ruoli, non nomi)
  status: done
  result: Entrambe inviate. Note leggere, non-pitch.
  next_step: Monitorare gli accept. DOPO accept + proof of work pubblicato -> follow-up DM con one-pager.
  notes: Pitch e email NON inviati di proposito (proof of work non ancora pubblico; nessun indirizzo email verificato).

- date: "[illustrativo]"
  route: proof of work
  action: Prodotti 3 asset.
  target: pubblico / outreach
  status: done (bozze, da numeri+approvazione Raffaele per pubblicare)
  result: >
    #3 case study "Yempik gira su Cowork" + bozza post LinkedIn (voce founder);
    #1 report "lo strumento no-code nei processi aziendali";
    one-pager PDF "B2B Adoption Program Italy" (impaginato, brand Yempik).
  next_step: Raffaele dà 2-3 numeri reali -> pubblicare #3, poi #1; allegare one-pager al follow-up.
  notes: file nella cartella proof_of_work/ (privata).

- date: "[illustrativo]"
  route: 2-3-4-6-7 (esecuzione parallela)
  action: Analisi ecosistema + numeri reali nel case study; one-pager rifatto a piena pagina; route parallele mentre l'accept è pendente.
  target: missione 001
  status: done
  result: >
    Case study #3 con conteggi reali (memoria, doc, pagine sito, commit, MCP, skill — valori [illustrativo])
    + stima riduzione tempo CONFERMATA dal founder ([illustrativo]). Post LinkedIn finale pronto. One-pager PDF ridisegnato.
    Nuovi asset: proposta evento "…for Business Operations" (Route 3) e risposte precompilate per le candidature (Route 2/4).
    Decisione: angolo "verticale sul tool no-code" confinato a questa missione (registrata nel decisions log).
  next_step: pubblicare proof of work; login per candidature; follow-up all'accept.
  notes: collegamenti alla sede locale ancora non accettati. Schedule settimanale (lunedì) controlla accept + news.

- date: "[illustrativo]"
  route: 3-4 (esecuzione su autorizzazione)
  action: Tentato invio candidatura al programma startup + ricerca canale reale per Route 3.
  target: vendor (programma startup + eventi)
  status: partial — boundary
  result: >
    Programma startup: il form non si renderizza in sessione + richiede login alla console.
    Non eseguo login/creo account al posto dell'utente -> NON inviata; pre-compilata per invio di Raffaele (2 min).
    Route 3: canali reali trovati = format "founder house" (prossima edizione da intercettare, forse Milano) + hosting community self-serve.
    Validazione forte: il vendor pubblica contenuti su "come i team marketing/finance usano lo strumento" = sta evangelizzando lo stesso cuneo.
    Nuovi contatti individuati per ruolo (head of startups; applied AI / devrel).
  next_step: Raffaele invia le candidature (login); monitorare il prossimo evento founder (schedule); valutare evento community self-hosted.
  notes: il post LinkedIn lo pubblica Raffaele.

- date: "[illustrativo]"
  route: 4 + 8 + 9
  action: Esito candidatura + nuova route eventi.
  target: vendor
  status: WIN
  result: >
    Programma startup ACCETTATO (welcome email). Benefit: priority invite eventi (founder/builder day, hackathon), community founder, live session, accesso a eventi community locali.
    Aggiunto "Member · programma startup" al one-pager e al follow-up come leva.
    Warm-intro via collegamenti LinkedIn comuni: SCARTATO (nessun contatto reale con quei profili).
    Nuova Route 9 in moto: evento community "…for Business Operations" presso uno spazio coworking a Milano (gratis membri) → pagina evento pronta. Gancio diretto verso la sede locale.
  next_step: Raffaele crea/pubblica l'evento + submit al canale community; poi si invita il team della sede locale. Monitorare il prossimo founder/builder day in Italia.
  notes: nuove route mappate (customer story, skill/plugin, cloud, nuovi hire locali) in route_map.

- date: "[illustrativo]"
  route: 14 — Community Ambassador
  action: INVIATA application al programma Community Ambassador del vendor.
  target: community team del vendor
  status: SUBMITTED → in attesa review/interview
  result: >
    Scoperto e applicato al programma ufficiale di community ambassador.
    Se accettato dà: finanziamento eventi + swag + promozione canali del vendor, crediti mensili sulla piattaforma,
    CANALE PRIVATO col team del vendor (≈ Definition of Done: linea diretta calda), pre-release, titolo pubblico usabile su LinkedIn.
    Risposte preparate; Raffaele ha compilato e inviato il form.
  next_step: attendere screening call; nel mentre agganciare l'evento community all'Ambassador. Aggiornare appena arriva risposta.
  notes: route più forte della missione finora — converte il cold outreach in relazione ufficiale supportata.
```

---

> *Sanitizzazione:* rimossi ragione sociale e numero di registro di Yempik, sede legale, l'elenco nominativo dei clienti del vendor, tutti i nomi di persona (sostituiti dai ruoli), il nome del partner locale e dello spazio coworking, gli importi dei programmi, i conteggi reali del case study (`[illustrativo]`) e tutti gli URL dei form. Restano Yempik, Raffaele, yempik.com.
