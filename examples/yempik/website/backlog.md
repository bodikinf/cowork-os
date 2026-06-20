> **EN —** Filled example (sanitized): Yempik's live-site backlog. Task structure kept; lead/testimonial names, company number, CPA/amounts → `[illustrativo]` / removed.
> **IT —** Esempio compilato (sanitizzato): backlog del sito Yempik. Struttura task mantenuta; nomi lead/testimonial, n. società, CPA/importi → `[illustrativo]` / rimossi.

---

# Yempik — Backlog Sito

> Task concreti sul sito in produzione (repository del sito, Next.js). Lo stato attuale dell'architettura è in `website_notes.md`.
> Convenzione: ogni task ha priorità **[ALTA] / [MEDIA] / [BASSA]** e l'obiettivo commerciale a cui è legato. Stati: `[ ]` da fare · `[~]` in corso · `[x]` fatto.

---

## Priorità ALTA — superficie commerciale che converte

- [ ] **[ALTA] Money page `/automazione-processi-aziendali`** *(SEO/Conversione)* — *non esiste*. È il cluster che ha **chiuso il primo lead** *(via canale chat, importo `[illustrativo]`)* e ha CPC bassi/concorrenza bassa. Pagina sul modello di `/agenti-ai-per-aziende`: H1 transazionale, cosa fa, 3 flussi concreti ("la fattura entra in mail ed esce in contabilità"), come funziona, prezzi, `serviceSchema` + `faqSchema` + `breadcrumbSchema`, link a `/prezzi` e case study.
  **Motivo:** catturare in organico la domanda che oggi paghiamo in paid + dare al gruppo Automazione una landing message-matched.
  **Fatto quando:** pagina live, indicizzata, con schema valido e link interni dal cluster guide.
- [ ] **[ALTA] Money page `/software-su-misura`** *(SEO/Conversione)* — *non esiste*. **Software house è il gruppo paid con CPA più basso** *(`[illustrativo]`)*, CPC di mercato alti: una money page organica su questi termini ha ROI strutturale. Stesso template (gestionali, integrazioni, "quando i gestionali pronti non bastano"), `serviceSchema`+FAQ+pricing+link interni.
  **Motivo:** intercettare "software house / software gestionale personalizzato / sviluppo software su misura" senza pagare CPC alti per clic.
- [ ] **[ALTA] 2° case study = Automazione** *(Contenuto)* — oggi i case study sono **2, entrambi voce**: la prova si concentra dove NON converte. Costruire 1 case study su un'automazione/processo (un workflow proprietario, se pubblicabile — vedi decisione sul citare progetti non pubblici).
  **Motivo:** spostare la prova dove la pipeline chiude.
- [ ] **[ALTA] Risolvere il testimonial in bozza già LIVE** *(Coerenza/Legale)* — la home ha `quoteDraft: true` per una citazione, ma il componente la renderizza comunque. O si conferma la pubblicabilità (chiude l'open question) o si nasconde dietro il flag.
  **Motivo:** rimuovere rischio legale/di fiducia sul principale social proof della home.

## Priorità MEDIA — coerenza, conversione, link interni

- [ ] **[MEDIA] Placeholder visibile su pagina live** *(Coerenza)* — riga "P.IVA: da confermare" su una pagina prodotto indicizzata → rimuovere la riga o sostituirla con l'entità legale corretta.
  **Motivo:** togliere un segnale di "sito non finito" su una pagina indicizzata.
- [ ] **[MEDIA] Link interni contestuali guide → commerciale** *(Conversione)* — le 8 guide ricevono già traffico organico. Aggiungere a fondo e inline CTA/link verso la money page pertinente + `/start` + case study (es. `come-misurare-il-roi-dell-ai` → `/prezzi`; `quale-processo-automatizzare-per-primo` → `/automazione-processi-aziendali`).
  **Motivo:** convertire il traffico informativo in lead.
- [ ] **[MEDIA] Elevare il canale chat come canale** *(Conversione)* — è l'**unico canale che ha chiuso**. Oggi è secondario (founder card, footer). Test: canale chat come CTA secondaria esplicita sulle money page e a fondo guide, oltre al form.
  **Motivo:** assecondare il comportamento di chi compra (n=1 → test, misurare).
- [ ] **[MEDIA] Coerenza entità "Made in Italy" ↔ entità legale** *(Coerenza)* — "software house italiana" + "Made in Italy" convivono con l'entità legale e "dati in UE". Allineare microcopy home (trust bar, garanzie) e `organizationSchema` per non confondere gli answer engine e gestire l'attrito di fatturazione.
  **Motivo:** togliere ambiguità nel momento della fiducia/acquisto.
- [ ] **[MEDIA] Nuova guida `come-automatizzare-linserimento-dati`** *(Contenuto/SEO)* — satellite del cluster automazione, ottimo aggancio alla money page `/automazione-processi-aziendali` (stesso tema "la fattura entra in mail ed esce in contabilità"). Struttura + copy già pronti in `contenuti-marketing/`. Richiede alcuni componenti articolo nuovi (calcolatore costo, mockup output, figura due modalità, albero decisionale).
  **Motivo:** catturare in organico «automatizzare inserimento dati / estrarre dati da fatture» e portare al cluster che converte.

## Priorità BASSA — rifiniture e GEO

- [ ] **[BASSA] Verificare la Conversion Label** sulla thank-you page (TODO nel codice). *Solo verifica* — le modifiche all'account Ads le fa la persona responsabile; il tracking è confermato funzionante.
- [ ] **[BASSA] Schema corretto per la pagina prodotto** — il `softwareApplicationSchema` ha default Education/LMS (tarati sull'altro prodotto verticale). Verificare/override per il voice agent (non LMS).
- [ ] **[BASSA] Aggiornare `llms.txt` + link interni** quando le money page automazione/software vanno live, così vengono citate dagli answer engine.
- [ ] **[BASSA]** Alt text e `<2s` su tutte le immagini nuove; OG dinamica delle nuove money page.

---

## Differenziatori (stato reale)
- [~] **Demo interattiva / "Provalo"** — già presente un voice assistant su `/start` e una live-call demo nei case study. Valutare se basta o se serve una mini-demo più visibile sopra la piega.
- [~] **Calcolatore ROI** — esiste come componente articolo nella guida ROI. Valutare se promuoverlo a micro-conversione su money page.
- [x] **Sezione "Quando NON serve l'AI"** — live come pagina (`/quando-non-serve-lai`), differenziatore di fiducia.

## Già risolto (storico, non cancellare)
- [x] **Form di contatto** — via email API, con honeypot + timing + captcha. Funzionante (lead reali arrivati).
- [x] **Canale chat reale** — numero server-side, mai in HTML crawlabile (anti-scrape).
- [x] **Entità legale** — inserita nel footer (sostituisce la P.IVA placeholder della vecchia spec).
- [x] **Privacy / Terms** — pagine `/privacy-policy` e `/terms-of-service` live.
- [x] **Tracciamento conversioni** — tag + thank-you page + email; conversioni reali registrate.
- [x] **Loghi clienti reali sotto la hero** — trust bar (resta da confermare il testimonial — vedi ALTA).

## Pagina "Formazione AI" (packaging del corso)
**Priorità: ALTA** (sblocca la nuova linea formazione B2B).
Contesto: il sito ha già un cluster di 8 guide d'autore che mappano 1:1 i moduli dell'AI Adoption Sprint, ma **manca una pagina-offerta** che le impacchetti in un corso vendibile. Task: creare `/formazione-aziende` con hero di valore, 4 moduli (ciascuno collegato alle guide pubblicate = prova del metodo), output del percorso, CTA "porta il corso in azienda", bonus SEO come hub di internal linking per il cluster articoli.

## Pagina `/partner` (canale partner B2B2B)
**Priorità: MEDIA** (sblocca il canale partner — vedi `business-development/`).
Contesto: nuova pagina di conversione rivolta ad **agenzie/web studio/software house** (non al cliente finale), per reclutarle come partner di delivery white-label. Audience e CTA diverse ("Diventa partner", non "Richiedi preventivo"). Riusare hero/process/pricing/case-study/cta + FAQ accordion. Bassa priorità SEO; linkare dal footer come "Per agenzie / Partner".
