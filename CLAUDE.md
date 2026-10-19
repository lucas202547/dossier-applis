# dossier-applis

Applis pédagogiques HTML autonomes (physique-chimie, lycée), publiées via GitHub Pages.

- Dépôt : https://github.com/lucas202547/dossier-applis
- En ligne : https://lucas202547.github.io/dossier-applis/<nom-du-dossier>/
- GitHub Pages : branche `main`, dossier `/ (root)` — déjà activé, rien à refaire.

## Structure

Une appli = un dossier = un fichier `index.html` autonome (HTML/CSS/JS dans le même fichier, pas de build).

```
dossier-applis/
├── AE04_preparation_solution_dissolution/index.html
├── AE06_vitesse_son/index.html
├── AE08_caracteristiques_son/index.html
├── corde-vibrante/index.html
├── lentille-convergente-1/index.html
└── onde-sonore/index.html
```

## Conventions

- Noms de dossiers : courts, sans espaces ni accents (lettres, chiffres, `_` ou `-`).
- Activités expérimentales : préfixe `AEnn_` (ex. `AE10_spectre_lumiere`).
- Le fichier de l'appli s'appelle toujours `index.html`.
- Pas de page d'accueil à la racine : l'adresse `/dossier-applis/` seule renvoie une 404, c'est normal.

## Ajouter une nouvelle appli

1. Créer le dossier (nom conforme aux conventions).
2. Y placer le fichier HTML renommé en `index.html`.
3. Commit (le push est fait par l'utilisateur) :
   ```powershell
   git add . ; git commit -m "Ajout <nom>" ; git push
   ```
4. Préparer la fiche JSON pour le site « Mes applis Éducation nationale » :
   ```json
   {
     "id": "slug-du-nom-de-l-appli",
     "nom": "Nom complet de l'appli",
     "description": "Description succincte en une phrase",
     "niveau": "seconde",
     "url": "https://lucas202547.github.io/dossier-applis/<nom-du-dossier>/",
     "authentification": {
       "requise": false
     }
   }
   ```
   URL sans `index.html` à la fin, avec le `/` final.
