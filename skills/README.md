> **EN —** Skills are specialized capabilities Claude can invoke (a LinkedIn editor, a document→spreadsheet extractor, office-file builders…). Most people don't know they exist — this folder catalogs the ones that pair with the kit and is where you keep your own. The installer proposes the relevant ones automatically.
> **IT —** Le skill sono capacità specializzate che Claude può invocare (un editor LinkedIn, un estrattore documenti→Excel, generatori di file Office…). Quasi nessuno sa che esistono — questa cartella cataloga quelle che si abbinano al kit ed è dove tieni le tue. L'installer propone in automatico quelle utili.

---

> **Where the bundled skills live.** The skills that ship with cowork-os (`cowork-os-core`, `knowledge-transfer`) are inside the plugin at [`plugins/cowork-os/skills/`](../plugins/cowork-os/skills/) and load automatically. **This `skills/` folder is the catalog plus room for your own custom skills**, which is why it is mostly just this README.

## Skills that pair with cowork-os · Skill che si abbinano

These are named so Claude can invoke them precisely. **Most are not bundled in this repo** (the first-party `knowledge-transfer` skill ships with the kit); the rest are separate Cowork skills. Claude uses whichever are installed; if a useful one is missing, it names it and points you to **Settings → Capabilities**.

| Skill | What it does | Claude reaches for it when |
|---|---|---|
| `knowledge-transfer` *(bundled)* | Interviews a person and builds the company brain (processes, rules with source, glossary) into the workspace. Runs on its own or via `/cowork-os:knowledge-transfer`. | onboarding, a key person leaving, standardizing a process |
| `linkedin-editor` | Turns any asset into ready-to-publish LinkedIn posts (8-step workflow). Also shipped here as a no-install workflow in `../linkedin/editor_workflow.md`. | "esegui l'editor su [asset]" |
| `document-data-extractor` | Pulls receipts / invoices / docs into a clean Excel table. | you want document data tabulated |
| `validation-outreach` | Cold messages that book *discovery* interviews (learning, not selling). | you want to talk to potential customers |
| `verification` | Proves code/work actually works before claiming it's done. | a technical task whose success is checkable |
| `youtube-transcript` | Clean transcript of a YouTube video. | you paste a video link / want its text |
| `docx` · `pptx` · `xlsx` · `pdf` | Build Word / PowerPoint / Excel / PDF deliverables. | a deliverable should be a doc / deck / sheet / PDF |
| `html-presentations` | High-end HTML slide decks with custom diagrams. | you want a designed presentation |
| `technical-decision-memory` | Institutional memory of past technical decisions. | revisiting an architecture/tooling choice |

> **Why not bundled:** third-party skills aren't ours to redistribute, and they evolve on their own. Cataloging + invoking them keeps the kit lightweight and always current.
>
> **Yempik's own skills** (e.g. `linkedin-editor`, `verification`) are published as standalone skills in the companion repo **`yempik-skills`** — cross-link them there rather than copying them here.

## Bring your own · Porta le tue

Keep a custom skill as its own subfolder with a `SKILL.md` inside — for example a folder `my-skill/` containing `SKILL.md`. Then either tell Claude when to use it, or add a row for it in `../capabilities.md` so the installer can propose it too.

> **Rule for Claude:** if a relevant skill is installed, just use it. If it isn't, name it and point the user to where capabilities are managed — never silently skip a capability the user doesn't know exists.
