# Template di follow-up — {{COMPANY}}

> Nella voce di {{RUOLO/NOME}}. La skill `pipeline-followup` usa questi template come base per le **bozze** (draft-only, in Gmail). Non sono script rigidi: la skill li adatta al thread reale e al contesto del deal. Fonte: intervista KT + rifinitura a mano.
> Tono: {{vedi context/tone_of_voice.md}} — {{es. diretto, breve, niente burocrazia, niente "buongiorno gentilissimo"}}.

---

## 1. Primo follow-up dopo proposta (silenzio breve)
**Quando:** proposta inviata, nessuna risposta oltre soglia.
**Obiettivo:** riportare a galla senza pressare.

```
Oggetto: {{riferimento al thread / proposta}}

Ciao {{nome}},
{{1 riga: aggancio al contesto reale — "ti avevo girato la proposta per X"}}.
{{1 riga: domanda semplice che apre — "hai avuto modo di darci un'occhiata? c'è qualcosa che ti torna meno?"}}
{{chiusura leggera con next step — "se è più comodo, ci sentiamo 10 minuti questa settimana"}}.
{{firma}}
```

## 2. Secondo follow-up (silenzio prolungato)
**Quando:** già un follow-up, ancora nessuna risposta.
**Obiettivo:** dare una via d'uscita facile, senza insistere.

```
Ciao {{nome}},
{{1 riga: rispetto del tempo — "non voglio intasarti la casella"}}.
{{la domanda binaria — "ha ancora senso per voi in questo periodo, o meglio riparlarne più avanti?"}}
{{firma}}
```

## 3. Deal fermo in negoziazione
**Quando:** trattativa avanzata bloccata su un punto (prezzo, timing, un decisore).
**Obiettivo:** sbloccare il punto specifico.

```
Ciao {{nome}},
{{1 riga sul punto aperto reale — dedotto dal thread/note}}.
{{proposta concreta per sbloccare — "possiamo fare X per andare incontro a Y"}}.
{{firma}}
```

## Regole per la skill quando genera la bozza
- Aggancia sempre al **thread reale** (leggi l'ultimo scambio), non a un template generico.
- Rispetta la **soglia e il max follow-up** in `rules.md`: se un deal ha già ricevuto il numero massimo, **non** generare un'altra bozza — segnalalo come "da marcare freddo".
- Mai inventare fatti sul deal (prezzi, promesse) non presenti nel thread o nelle note CRM.
- Output = **bozza in Gmail**, mai invio. Lascia il campo destinatario/oggetto pronti ma non spedire.
