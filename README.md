# ClairStart — waiting page

Page d'attente statique servie sur **clairstart.com** en attendant la mise en ligne du site
complet (repo `clear-light-spark`).

- Fichier unique, sans dépendance : `index.html` (CSS + JS inline, aucune requête externe).
- Bilingue FR/EN (toggle, langue mémorisée en `localStorage`, détection navigateur au 1er passage).
- Direction visuelle « Piste C » de ClairStart : sombre chaleureux, glow ambré, titre qui passe
  du flou au net. `prefers-reduced-motion` respecté.
- Hébergement : **GitHub Pages** (HTTPS automatique).

## Aperçu local

```
node serve.cjs        # http://localhost:5281
```

## Remplacer par le site complet

Quand le vrai site part en production (Vercel), repointer le DNS de `clairstart.com` vers Vercel
et désactiver GitHub Pages ici — ou garder ce repo comme page de secours.
