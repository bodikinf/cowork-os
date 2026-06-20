# Publishing this repo · Pubblicare questo repo

> **EN —** How to put this folder on GitHub. ~2 minutes.
> **IT —** Come mettere questa cartella su GitHub. ~2 minuti.

## EN

**1. Start with a clean git history** (recommended — the folder ships with a build-time commit; re-initing on your machine gives you a pristine one as the author):
```bash
cd cowork-os
rm -rf .git
git init
git add -A
git commit -m "cowork-os: initial release"
```

**2. Create an empty repo on GitHub** — no README/license, this folder already has them. Use the name you and your co-founder agree on (working name: `cowork-os`).

**3. Connect and push:**
```bash
git remote add origin https://github.com/<your-account>/<repo-name>.git
git branch -M main
git push -u origin main
```

**4. Final safety check** — make sure no private file slipped in:
```bash
git ls-files | grep -iE 'client|accounting|preventiv|contratt|\.env' || echo "clean"
```
This package ships only templates and sanitized examples. Keep it that way.

## IT

**1. Parti con una history git pulita** (consigliato — la cartella include un commit di build; re-inizializzando sul tuo Mac ne ottieni uno pulito a tuo nome):
```bash
cd cowork-os
rm -rf .git
git init
git add -A
git commit -m "cowork-os: initial release"
```

**2. Crea un repo vuoto su GitHub** — senza README/license, ci sono già. Usa il nome che decidi col tuo socio (nome di lavoro: `cowork-os`).

**3. Collega e pusha:**
```bash
git remote add origin https://github.com/<tuo-account>/<nome-repo>.git
git branch -M main
git push -u origin main
```

**4. Controllo finale di sicurezza** — verifica che non sia entrato nessun file privato:
```bash
git ls-files | grep -iE 'client|accounting|preventiv|contratt|\.env' || echo "pulito"
```
Questo pacchetto contiene solo template ed esempi sanitizzati. Mantienilo così.
