# Dérive Poétique

Application statique prête à publier sur GitHub Pages.

## Mise en ligne

1. Crée un nouveau dépôt GitHub.
2. Envoie le contenu de ce dossier à la racine du dépôt.
3. Vérifie que le fichier principal s'appelle `index.html`.
4. Sur GitHub, ouvre **Settings > Pages**.
5. Dans **Build and deployment**, choisis **Deploy from a branch**.
6. Sélectionne la branche **main** et le dossier **/(root)**.
7. Enregistre. GitHub Pages publiera ensuite le site.

L'URL finale aura généralement cette forme :

`https://<ton-nom-utilisateur>.github.io/<nom-du-repo>/`

## Développement local

Tu peux tester localement avec :

```bash
python3 -m http.server 8000
```

Puis ouvre :

`http://localhost:8000/`

## Contenu

- `index.html` : l'application
- `.nojekyll` : évite certains traitements GitHub Pages
