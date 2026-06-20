# cowork.config — fill these once

> **EN —** The single source of truth for every `{{PLACEHOLDER}}` used across the templates. Copy this to `cowork.config.md`, fill it in, and keep it private if you wish.
> **IT —** L'unica fonte di verità per ogni `{{PLACEHOLDER}}` usato nei template. Copia questo file in `cowork.config.md`, compilalo, e tienilo privato se vuoi.

| Placeholder | Meaning · Significato | Your value · Il tuo valore |
|---|---|---|
| `{{COMPANY}}` | Company / brand name · Nome azienda/brand | _e.g._ Yempik |
| `{{COMPANY_ONE_LINER}}` | One sentence: what you do · Una frase: cosa fai | _e.g._ software house — software, automazioni, agenti AI |
| `{{FOUNDER}}` | Personal-brand first name · Nome (personal brand) | _e.g._ Raffaele |
| `{{WEBSITE}}` | Main website · Sito principale | _e.g._ yempik.com |
| `{{WEBSITE_REPO}}` | Website repo name (if any) · Repo del sito | |
| `{{ICP}}` | Ideal customer profile · Cliente ideale | |
| `{{CATEGORY}}` | Mental category you want to own · Categoria mentale da presidiare | |
| `{{SERVICE_1}}` … | Services / offers · Servizi / offerte | |
| `{{CHANNEL}}` | Primary marketing channel · Canale marketing primario | |
| `{{KPI_1}}` … | Key metrics you track · Metriche chiave | |
| `{{TARGET}}` | A mission target (org/ecosystem) · Target di una missione | |

**Third-party placeholders** — never hard-code a real name in a public file:

| Placeholder | Meaning |
|---|---|
| `{{CLIENT}}` | A client |
| `{{LEAD}}` | A sales lead / prospect |
| `{{PARTNER}}` | A partner |
| `{{METRIC}}`, `{{NUMBER}}`, `{{AMOUNT}}`, `{{DATE}}` | Any figure / date |

**Module-specific placeholders** — used inside the flagship modules:

| Placeholder | Used in | Meaning |
|---|---|---|
| `{{PRODUCT}}` | products/ | An owned product name |
| `{{COMPETITOR_TYPE}}` | context/positioning | A *type* of competitor (never a real name) |
| `{{CONTACT_EMAIL}}` | context, website | Public contact email |
| `{{POSITIONING_ANGLE}}`, `{{CATEGORY_THESIS}}` | linkedin/ | Your angle and the category you claim |
| `{{PILLAR_1}}`…`{{PILLAR_4}}` | linkedin/ | The 4 content pillars |
| `{{KPI_POSTS}}`, `{{KPI_COMMENTS_OUT}}`, `{{KPI_LEADS}}` | linkedin/ | LinkedIn KPI targets |
| `{{WINDOW_AM}}`, `{{WINDOW_LUNCH}}` | linkedin/ | Posting time windows |
| `{{TASK_NAME_TREND}}`, `{{TASK_NAME_RADAR}}` | linkedin/, scheduled-tasks/ | Names of your scheduled automations |
| `{{KEYWORD_IT_1}}`, `{{KEYWORD_EN_1}}`, `{{KEYWORD_QUERY_1}}` | linkedin/, scheduled-tasks/ | Search keywords for trend/radar |
| `{{MISSION}}`, `{{MISSION_SLUG}}` | missions/, scheduled-tasks/ | An active mission and its folder name |
| `{{GOAL}}`, `{{TARGET_OUTCOME}}`, `{{LANDING_PAGE}}` | missions/ | A mission's goal, outcome, and landing page |

> Tip: keep your filled `cowork.config.md` and any real client folders out of the public repo (see `.gitignore`).
