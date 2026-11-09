# Journal de coulage · Fondations WTG

Application web installable (PWA) pour les journées de coulage des fondations d'éoliennes. Fonctionne hors ligne une fois installée ; les données restent sur le téléphone ; le rapport Word (.docx) est généré sur le téléphone.

- `index.html` : application vierge
- `exemple.html` : exemple Gouzeaucourt
- Pas de serveur, pas de compte, pas de build.

## Publier sur GitHub Pages
1. Sur github.com : **New repository** → nom `journal-coulage` → **Private** ou Public (voir note) → Create.
2. **Add file → Upload files** : glissez tout le contenu de ce dossier (y compris `icons/`, `.nojekyll`) → Commit.
3. **Settings → Pages** → *Build and deployment* : Source = **Deploy from a branch**, Branch = `main`, dossier `/ (root)` → Save.
4. Après 1 à 2 minutes l'adresse apparaît : `https://<votre-compte>.github.io/journal-coulage/`

Note : GitHub Pages sur dépôt privé exige un compte payant (Pro/Team/Enterprise). Avec un dépôt public, l'application (et le logo EDF) est lisible par toute personne connaissant l'adresse ; aucune donnée de chantier n'y est stockée.

## Installer sur le téléphone
- **iPhone (Safari)** : ouvrir l'adresse → bouton Partager → **Sur l'écran d'accueil**.
- **Android (Chrome)** : ouvrir l'adresse → menu ⋮ → **Installer l'application** (ou Ajouter à l'écran d'accueil).

Ouvrir l'application une fois avec du réseau, puis elle marche hors ligne sur le chantier.

## Mise à jour
Remplacer les fichiers dans le dépôt (Upload files, même nom). Au prochain lancement avec réseau, la nouvelle version est chargée. En cas de doute, incrémenter `V` dans `sw.js` (`coulage-v2`).

## Données
Fiches : stockage local du navigateur ; photos : IndexedDB. Effacer les données du site ou désinstaller l'application supprime les fiches : exporter le rapport Word avant.
