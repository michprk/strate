# Strate, jardins à Bruxelles (site d’exemple)

Site d’exemple **Premium** conçu par [M&S Design](https://michprk.github.io/msdesign.be/), Bruxelles.
Strate est une **entreprise fictive** : ses jardins, ses prix, ses dates et son atelier sont inventés.

En ligne : https://michprk.github.io/strate/

## L’idée

Un jardin se comprend par sa coupe. On entre (avec ou sans le son), on arrive dans un jardin
bruxellois en 3D vu à travers une arche, puis chaque cran de molette joue un chapitre entier :

1. **Le jardin** : pelouse au vent (elle s’écarte sous la souris), amélanchier d’automne, buis,
   pierre bleue, haie d’ifs, murs en brique.
2. **Le sol** : la caméra passe au ras de l’herbe et descend dans la coupe : terre végétale, limon,
   argile, sable bruxellien. Les racines poussent.
3. **L’eau** : les gouttes s’infiltrent jusqu’à la nappe.
4. **Les étages** : le jardin s’écarte en strates (sol, couvre-sols, vivaces, arbustes, arbre).

Ensuite : trois jardins en plans au trait, les prix sur un calendrier de semaines, la roue des
saisons (aiguille sur la date du jour) et un formulaire de démonstration (rien n’est envoyé).

## Technique

- HTML, CSS et JavaScript sans outil de build ; Three.js r160 et Lenis 1.3 dans `vendor/`.
- `js/garden.js` : toute la scène est générée par le code (aucun modèle 3D, aucune photo).
- `js/sound.js` : ambiance synthétisée en Web Audio (vent, oiseaux, puis sol assourdi et gouttes),
  très discrète, seulement après le choix « Entrer dans le jardin » ; « Couper le son » en bas de page.
- `js/page.js` : chapitres, écran d’entrée, menu, plans, calendrier.
- Animations complètes par défaut ; « Réduire les animations » en bas de page ou `?motion=reduce`.
- `?intro=0` saute l’écran d’entrée ; `?qa=0..3` fige un chapitre pour les captures.
- Polices Gloock, Hanken Grotesk, DM Mono (SIL OFL), Three.js et Lenis (MIT) : voir `licenses/`.

Les sources (plans, calendrier, outils de capture) sont dans l’atelier de M&S Design ;
ce dépôt est la copie publiée, exportée par `_msdesign-src/strate/export.mjs`.
