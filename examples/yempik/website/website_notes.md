> **EN —** Filled example (sanitized): how yempik.com is built. Architecture/GEO method kept; product names generalized, company number/testimonial names → `[illustrativo]` / removed.
> **IT —** Esempio compilato (sanitizzato): com'è fatto yempik.com. Metodo architettura/GEO mantenuto; nomi prodotti generalizzati, n. società/testimonial → `[illustrativo]` / rimossi.

---

# Yempik — Note sito (produzione)

> Com'è fatto il sito in produzione e come è impostato. I task aperti stanno in `backlog.md`.
> Repo: il repository del sito (Next.js / React / Tailwind). Dominio: `yempik.com`.

## Architettura reale (due superfici + cluster contenuti)
Il sito **non è** una landing a pagina singola. È un sito multi-pagina con due ruoli distinti:

- **Homepage `/` = hub di credibilità** per traffico brand/organico/referral. Ha menu, dropdown Prodotti, sezioni: hero "In produzione, non in slide" · trust bar loghi · 3 servizi · case study in evidenza · verticale Agenti vocali · metodo 4 step · perché Yempik + garanzie · pacchetti · prodotti · CTA/form + founder card. Copy in `website/homepage_copy.md`.
- **Landing `/start` = macchina di conversione del traffico paid.** È qui che puntano tutti gli annunci Google Ads. Form (via email API) + canale chat + voice assistant demo + tracking conversioni.

**Pagine servizi / money page:** `/servizi` (hub), `/agenti-ai-per-aziende` (money page agenti), `/prezzi`. ⚠️ **Mancano** money page per **automazione** e **software su misura** (i due cluster che convertono — vedi `backlog.md` ALTA).

**Case study:** `/case-studies` + `/case-studies/[id]`. Oggi **2 case study, entrambi voce** *(settori [illustrativo])*. Nessun case study automazione/software.

**Prodotti:** una pagina prodotto per il voice agent verticale in lancio; un secondo prodotto verticale è off-domain.

**Cluster SEO/GEO (8 guide):** pillar `/come-integrare-agenti-ai-in-azienda` + satelliti (`quale-processo-automatizzare-per-primo`, `come-standardizzare-un-processo`, `come-far-adottare-lai-al-team`, `come-misurare-il-roi-dell-ai`, `ai-governance-per-le-pmi`, `quando-non-serve-lai`, `confronto/agente-ai-vs-chatbot-vs-no-code`) + archivio `/blog`. Ricevono già traffico organico.

## Fondazione GEO / answer engine (forte e matura)
- **JSON-LD completo:** Organization, WebSite, Service (+AggregateOffer con prezzi "da"), FAQPage, Article, Blog, BreadcrumbList, Person, SoftwareApplication.
- **`public/llms.txt`** curato e aggiornato (sintesi citabile, servizi, prezzi, definizioni, FAQ). Da tenere sincronizzato con le FAQ.
- **`robots`** con allowlist esplicita dei crawler AI (GPTBot, ClaudeBot, PerplexityBot, Google-Extended, CCBot…). **IndexNow** attivo. OG dinamiche per articolo.
- **FAQ GEO-ready:** risposte 40–60 parole pensate per citazione verbatim, replicate in `llms.txt`.

## Principi di conversione `/start` (regole d'oro, ancora valide)
Un obiettivo: lead qualificati. CTA d'azione ("Richiedi un preventivo", mai "Invia"), ripetuta uguale. Prova (loghi) subito sotto la hero. Prezzi "a partire da" come ancora che filtra i lead. Microcopy anti-ansia vicino al form ("Rispondiamo entro 24h · Nessun impegno"). Mobile-first con CTA sticky. Coerenza con `context/tone_of_voice.md` (niente cliché AI: viola, robot, dashboard finte).

## SEO / meta (impostati)
- Homepage title: *Yempik · Agenti AI, automazioni e software su misura in Italia*
- Sitemap dinamica con core + prodotti + articoli + case study. Canonical su `https://www.yempik.com`.

## Coerenza da tenere d'occhio
- **"Made in Italy / software house italiana" ↔ entità legale + "dati in UE".** Convivono ma vanno formulati con cura (answer engine + fatturazione verso PMI italiane). Vedi `backlog.md` MEDIA e `decisions/open_questions.md`.
- **Testimonial** marcato `quoteDraft: true` ma **renderizzato in produzione**: confermare pubblicabilità o gating.
- Placeholder residuo "P.IVA: da confermare" su una pagina prodotto indicizzata.

**Disallineamento strategico chiave:** la superficie di contenuto (narrativa + case study) è centrata su **agenti AI / voce**, ma la domanda che **converte** in paid è **software house + automazione**. Riequilibrare con money page e case study su quei cluster (vedi `backlog.md`).

## I contenuti pubblicati SONO il corso (asset di vendita)
Il cluster pillar+satelliti già live (8 guide d'autore, founder Raffaele) copre per intero il programma dell'AI Adoption Sprint. Implicazione marketing: risolve il dubbio "come demistifico il valore della formazione" → il valore è già dimostrato e pubblico, non va affermato a parole. Outreach: si manda la guida + "in 16h te lo faccio fare sul tuo processo". Manca solo la pagina-offerta che li converte in corso (vedi `website/backlog.md`).

## Il logo Yempik è un wordmark tipografico (nessun file logo nel repo)
Il marchio è generato via codice come wordmark `yempik` + punto accent, e come icona/monogramma `y.` per favicon/app-icon. Non esiste un file immagine del logo ufficiale.
- **Parametri brand:** font **Geist Sans** (variabile, wordmark peso 500, monogramma 600); colori **ink `#0A0A0A`**, **accent `#E35B2D`**, **cream/bg `#FAFAF8`**.
- **Gap segnalato:** manca un asset logo ufficiale versionato. Valutare se aggiungere `brand/logo/` come fonte unica condivisa per usi esterni.

## Niente finte dashboard — design/mockup veri, non screenshot brutti `[DECISIONE]`
Bandire qualsiasi "finta dashboard" (cruscotti con dati inventati, barre/gauge decorative, icone refresh che fingono dati live). Ribadisce e rafforza la regola già in `context/tone_of_voice.md`. Direzione di design: dove serve un visivo, **prediligere design e mockup curati e reali** — mai screenshot brutti né dati finti travestiti da prodotto. Se si mostra un dato, deve essere vero e con fonte.
