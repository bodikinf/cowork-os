> **EN —** How the live site is built and set up: architecture, surfaces, SEO/GEO, conversion rules. Update when the site structure changes. Open tasks live in `backlog.md`.
> **IT —** Com'è fatto il sito in produzione e come è impostato: architettura, superfici, SEO/GEO, regole di conversione. Aggiornalo quando cambia la struttura. I task aperti stanno in `backlog.md`.

---

# {{COMPANY}} — Note sito (produzione)

> Com'è fatto il sito e come è impostato. I task aperti stanno in `backlog.md`.
> Repo: `{{WEBSITE_REPO}}` ({{STACK_SITO — es. Next.js / React / Tailwind}}). Dominio: `{{WEBSITE}}`. Aggiornato: {{DATE}}.

## Architettura (superfici + cluster contenuti)
> Descrivi i ruoli delle pagine, non solo la lista. Una pagina = un lavoro.
- **Homepage `/` = hub di credibilità** per traffico brand/organico/referral. Sezioni: {{elenco sezioni}}.
- **Landing `/start` = macchina di conversione del traffico paid.** È qui che puntano tutti gli annunci. Form + canale chat + tracking conversioni.
- **Pagine servizi / money page:** {{elenco}}. ⚠️ Segnala quali **mancano** (es. money page per i cluster che convertono — vedi `backlog.md`).
- **Case study:** {{elenco}}. Segnala se la prova è concentrata dove **non** converte.
- **Cluster SEO/GEO:** pillar `{{PILLAR_SLUG}}` + satelliti ({{elenco}}) + archivio `/blog`.

## Fondazione GEO / answer engine
> Cosa rende il sito citabile dai motori di risposta.
- **JSON-LD completo:** Organization, WebSite, Service (+ prezzi "da"), FAQPage, Article, BreadcrumbList, Person, …
- **`public/llms.txt`** curato (sintesi citabile, servizi, prezzi, FAQ). Tienilo sincronizzato con le FAQ.
- **`robots`** con allowlist esplicita dei crawler AI. **IndexNow** attivo.
- **FAQ GEO-ready:** risposte 40–60 parole pensate per citazione verbatim.

## Principi di conversione `/start` (regole d'oro)
Un obiettivo: lead qualificati. CTA d'azione ("{{CTA_TEXT}}", mai "Invia"), ripetuta uguale. Prova (loghi) subito sotto la hero. Prezzi "a partire da" come ancora che filtra i lead. Microcopy anti-ansia vicino al form. Mobile-first con CTA sticky. Coerenza con `context/tone_of_voice.md` (niente cliché: viola, robot, dashboard finte).

## SEO / meta (impostati)
- Homepage title: *{{HOMEPAGE_TITLE}}*
- Sitemap dinamica con core + prodotti + articoli + case study. Canonical su `https://www.{{WEBSITE}}`.

## Coerenza da tenere d'occhio
> I punti dove il messaggio e la realtà legale/tecnica potrebbero confliggere.
- {{CONSISTENCY_ITEM_1 — es. "Made in Italy" ↔ entità legale; "dati in UE"}}
- {{CONSISTENCY_ITEM_2 — es. testimonial marcati bozza ma renderizzati live}}
- Placeholder residui su pagine indicizzate (es. "P.IVA: da confermare").

**Disallineamento strategico chiave:** se la superficie di contenuto è centrata su un tema ma la domanda che **converte** è su un altro, riequilibra con money page e case study sui cluster che chiudono (vedi `backlog.md`).
