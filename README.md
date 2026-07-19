# Portfolio Data — Site statique

Site vitrine du portfolio, prêt à déployer sur GitHub Pages. Pas de build step (HTML/CSS pur) — aucune installation nécessaire.

## Structure

```
portfolio-site/
├── index.html                       # Accueil : hero + ledger des 5 projets
├── about.html                       # Page "À propos" / branding
├── projects/
│   └── rfm-segmentation.html        # Étude de cas complète (projet 1/5)
├── assets/
│   ├── css/style.css
│   ├── img/rfm/                     # Visuels du projet RFM
│   └── cv.pdf                       # ⚠️ À AJOUTER : ton CV au format PDF
└── README.md
```

## ⚠️ Avant de déployer — à personnaliser

1. **Ajouter ton CV** dans `assets/cv.pdf` (le lien existe déjà dans la nav et le footer, mais le fichier n'y est pas encore).
2. **Remplacer les liens réseaux sociaux** — actuellement des placeholders (`https://github.com/`, `https://linkedin.com/`, `ton.email@example.com`) dans `index.html`, `about.html` et `projects/rfm-segmentation.html`.
3. **Remplacer les liens "Voir le code sur GitHub"** sur la page RFM par l'URL réelle de ton repo `rfm-customer-segmentation`.
4. Au fur et à mesure que tu termines les 4 autres projets (MACRO, CREDIT, ALLOC, PRED), passe leur ligne dans `index.html` de `ledger-row is-pending` à `ledger-row is-live` avec un lien `<a>` vers une nouvelle page dans `projects/`, sur le modèle de `rfm-segmentation.html`.

## Déployer sur GitHub Pages

```bash
# Depuis ce dossier
git init
git add .
git commit -m "Portfolio v1 — projet RFM"
git branch -M main
git remote add origin https://github.com/<ton-username>/<ton-username>.github.io.git
git push -u origin main
```

Si le repo s'appelle `<ton-username>.github.io`, le site sera automatiquement disponible à `https://<ton-username>.github.io/` — sans configuration supplémentaire.

Sinon (repo avec un autre nom) : Settings → Pages → Source → Branch `main` → `/root`. Le site sera à `https://<ton-username>.github.io/<nom-du-repo>/`.

## Tester en local

```bash
python3 -m http.server 8000
# puis ouvrir http://localhost:8000
```
