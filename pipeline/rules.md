# Regole di vendita — {{COMPANY}}

> Catturato con `/cowork-os:knowledge-transfer` il {{DATA}} · Fonte: intervista con {{RUOLO/NOME}} (es. il commerciale) · Ultimo aggiornamento: {{DATA}}
> Regola d'oro: scrivi la versione **reale** del processo, non quella ufficiale. Le automazioni (`pipeline-deal-radar`, skill `pipeline-followup`) leggono QUESTO file: se una regola è vuota, chiedono invece di inventare.

---

## CRM di riferimento
- Sistema: {{es. Pipedrive}} · Pipeline/e osservate: {{nome pipeline}}.

## Stadi reali della pipeline
> Come sono chiamati DAVVERO nel CRM e cosa significano operativamente (non la teoria del funnel).

| Stadio (nome nel CRM) | Cosa significa davvero | Prossima azione tipica |
|---|---|---|
| {{Lead}} | {{...}} | {{...}} |
| {{Contattato}} | {{...}} | {{...}} |
| {{Discovery}} | {{...}} | {{...}} |
| {{Proposta inviata}} | {{...}} | {{...}} |
| {{Negoziazione}} | {{...}} | {{...}} |
| {{Chiuso vinto / perso}} | {{...}} | {{—}} |

## Cosa vuol dire "fermo" (deal stuck)
> La definizione che fa scattare il deal radar. Sii specifico.

- Un deal è **fermo** se: {{es. è in "Proposta inviata" da più di X giorni senza attività registrata}}.
- Un deal ha una **prossima azione mancante** se: {{es. non ha né data di follow-up né attività aperta}}.

## Soglia no-reply (per il follow-up)
> Dopo quanti giorni di silenzio si prepara una bozza di follow-up. Può variare per tipo di deal.

- Default: **{{5}} giorni lavorativi** senza risposta dopo l'ultimo messaggio inviato.
- Override per tipo:
  - Deal caldi / short cycle ({{es. valore < X, o stadio Negoziazione}}): {{3}} giorni.
  - Deal lunghi / enterprise ({{...}}): {{7-10}} giorni.
- Massimo numero di follow-up prima di fermarsi / marcare come freddo: {{es. 3}}.

## Campi Pipedrive effettivamente usati
> Solo i campi che la persona guarda o compila davvero. Ignora il resto.

- Stato/stadio: {{campo}}
- Prossima attività / data follow-up: {{campo}}
- Priorità: {{campo o "non usato"}}
- Valore: {{campo}}
- Referente / persona: {{campo}}
- Note / contesto: {{campo}}
- {{campo custom rilevante}}: {{...}}

## Criteri di priorità
> Come si decide cosa viene prima nel radar quando ci sono tanti deal.

- Ordina per: {{es. data follow-up crescente, poi valore decrescente}}.
- In cima vanno sempre: {{es. deal in Negoziazione con scadenza, deal ad alto valore fermi}}.

## Cosa NON fare mai (paletti)
- Non spostare stadi nel CRM in autonomia. {{conferma/adatta}}
- Non inviare email/messaggi: solo bozze. {{conferma}}
- Non ricontattare {{tipi di contatto da escludere: es. clienti in pausa concordata, deal persi}}.

## Domande aperte
- {{cosa resta da chiarire sul processo}} → registrate in `decisions/open_questions.md`.
