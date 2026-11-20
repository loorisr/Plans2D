# Plans 2D

Éditeur de plans 2D (murs, portes, fenêtres, radiateurs, cotes) qui tourne entièrement dans le navigateur. Tout tient dans un seul fichier `index.html` : pas de dépendances, pas de serveur, pas d'étape de build.

**Démo en ligne : <https://loorisr.github.io/Plans2D/>**

## Démarrage

Utilisez la [version en ligne](https://loorisr.github.io/Plans2D/), ou ouvrez `index.html` dans un navigateur récent :

```bash
xdg-open index.html     # Linux
open index.html         # macOS
```

Vous pouvez aussi le servir en local avec `python3 -m http.server`.

## Fonctionnalités

- **Murs** : tracé point par point avec saisie de la longueur au clavier (`420`, ou `420<30` pour donner un angle), fermeture d'une pièce en recliquant le premier point. La ligne de tracé peut être la face intérieure, l'axe ou la face extérieure, et l'épaisseur se règle.
- **Ouvertures** : fenêtres (largeur, hauteur, allège), portes (sens d'ouverture, charnière) et radiateurs, placés sur les murs.
- **Cotes** : cotes intérieures et extérieures automatiques, cotes des ouvertures, cotes libres. Un double-clic sur une cote permet de modifier la longueur du mur.
- **Pièces** : textes et noms de pièces, calcul automatique des surfaces.
- **Accroches** : grille, angles à 45°/90°, accroche aux nœuds, aux angles, aux faces et aux alignements.
- **Édition** : sélection, déplacement, copier/coller/dupliquer, décalage au clavier, annuler/rétablir.
- **Export** : SVG, PNG, DXF (en m ou en cm) et impression/PDF à l'échelle 1:50 ou 1:100, ou ajustée à la page (A4 ou A3).
- **Sauvegarde** : enregistrement automatique dans le `localStorage` du navigateur, et export/import au format `.json`.
- Thème clair ou sombre selon le système, mise en page adaptée aux petits écrans.

## Outils et raccourcis

| Touche | Action |
|---|---|
| `V` `W` `F` `D` `R` `C` `T` | Outils Sélection, Mur, Fenêtre, Porte, Radiateur, Cote libre, Texte |
| `Entrée` | Valider une longueur / terminer le tracé |
| `Retour arrière` | Retirer le dernier point |
| `Maj` | Angle libre / sans grille |
| `Tab` (outil Mur) | Changer la ligne de tracé (côté du mur / axe) |
| `420<30` | Saisir une longueur et un angle |
| Molette | Zoom |
| `Espace` + glisser | Déplacer la vue |
| `Origine` | Tout afficher |
| `X` / `H` | Inverser le sens d'ouverture / la charnière |
| Flèches | Décaler de 1 cm (10 cm avec `Maj`) |
| `Ctrl+C` / `Ctrl+V` / `Ctrl+D` | Copier / coller / dupliquer |
| `Suppr` | Effacer la sélection |
| `Ctrl+Z` / `Ctrl+Y` | Annuler / rétablir |
| `Ctrl+S` / `Ctrl+O` | Enregistrer / ouvrir un `.json` |
| Double-clic sur une cote | Modifier la longueur |

## Prise en main

1. Prenez l'outil **Mur** (`W`), cliquez un premier angle, tapez une longueur puis `Entrée`, et continuez ainsi.
2. Recliquez le premier point pour fermer la pièce.
3. Ajoutez des fenêtres (`F`), des portes (`D`) ou des radiateurs (`R`) en cliquant sur un mur.
4. Sélectionnez un élément (`V`) pour modifier ses dimensions dans le panneau de droite.
5. Exportez le plan ou enregistrez-le en `.json`.

Quand rien n'est sélectionné, le panneau de droite affiche les réglages du plan : épaisseurs, accroches, affichage des cotes, unité, dimensions par défaut et options d'export. Le bouton **Charger l'exemple** ouvre un plan de démonstration.
