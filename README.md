# DAARK³ — site web

Site statique (HTML/CSS/JS sans dépendance), une seule page : Hero, The Place, Coffee, Visit, Footer.

## Structure
- `index.html` — le site prêt à mettre en ligne (généré)
- `src/index.html` — le gabarit à modifier (design, textes)
- `content/menu.json` — la sélection de cafés (source unique)
- `build.py` — injecte le menu dans le gabarit : `python3 build.py`
- `assets/img/` — photos optimisées (WebP 640/1200 + JPG de secours)
- `preview/` — version pour l'aperçu claude.ai (générée)

## Changer la sélection de saison
1. Modifier `content/menu.json` (saison, catégories, cafés : type, roaster, name, origin, process, notes).
2. Lancer `python3 build.py`.
3. Mettre en ligne `index.html` + `assets/`.

## À vérifier avant mise en ligne
- Les balises `og:image` et `canonical` supposent que le site est hébergé sur https://daarkcoffee.com.
- Aucun horaire n'est affiché (non vérifiable) : le site renvoie vers Instagram. Ajouter les horaires dans `src/index.html` (section Visit) et dans le JSON-LD une fois confirmés.
