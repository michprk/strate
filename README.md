# Strate, jardins à Bruxelles (site d’exemple)

Site d’exemple **Premium** conçu par [M&S Design](https://michprk.github.io/msdesign.be/), Bruxelles.
Strate est une **entreprise fictive** : ses jardins, ses prix, ses dates et son atelier sont inventés.

En ligne : https://michprk.github.io/strate/

## L’idée

Un jardin se comprend par sa coupe. On entre (avec ou sans le son) sur une vraie photo de massif
d’automne en plein écran ; puis chaque cran de molette joue un chapitre entier, en 3D :

1. **Le jardin** : la photo s’agrandit et s’efface ; derrière, un jardin bruxellois en 3D (pelouse au vent,
   amélanchier d’automne, buis, pierre bleue, haie d’ifs, murs en brique).
2. **Le sol** : la caméra passe au ras de l’herbe et descend dans la coupe : terre végétale, limon,
   argile, sable bruxellien. Les racines poussent.
3. **L’eau** : les gouttes s’infiltrent jusqu’à la nappe.
4. **Les étages** : le jardin s’écarte en strates (sol, couvre-sols, vivaces, arbustes, arbre).

Ensuite : trois jardins en plans au trait, les prix sur un calendrier de semaines et la roue des
saisons (aiguille sur la date du jour).

**Page Saisons** (`saisons.html`) : un lieu réel, l’étang du Bois de la Cambre à Bruxelles, au printemps,
en été, en automne et en hiver (photos Wikimedia Commons, CC BY / CC BY-SA, créditées en pied de page).
Un cran de molette par saison, un curseur, le clavier, ou la photo qu’on fait glisser.

**Page Jardins** (`jardins.html`) : quatre vrais jardins publics de Bruxelles qui inspirent l’atelier
(jardins Van Buuren, abbaye de la Cambre, Jardin botanique, parc Josaphat). Ils ne sont pas l’œuvre de
Strate. Photos presque plein écran, commune au survol ; au clic, la photo s’ouvre en grand avec un
cadre de repérage, puis la fiche du lieu.

**Page Contact** (`contact.html`) : un plan de jardin se dessine au crayon, ses lignes deviennent
celles du formulaire, les champs arrivent un à un ; à l’envoi, une pousse sort de terre
(démonstration : rien n’est envoyé).

## Technique

- HTML, CSS et JavaScript sans outil de build ; Three.js r160 et Lenis 1.3 dans `vendor/`.
- `js/garden.js` : toute la scène est générée par le code (aucun modèle 3D, aucune photo).
- `js/sound.js` : ambiance synthétisée en Web Audio (vent, oiseaux, puis sol assourdi et gouttes),
  très discrète, seulement après le choix « Entrer dans le jardin » ; « Couper le son » en bas de page.
- `js/page.js` : chapitres, écran d’entrée, menu, plans, calendrier.
- Animations complètes par défaut ; « Réduire les animations » en bas de page ou `?motion=reduce`.
- `?intro=0` saute l’écran d’entrée ; `?qa=0..3` fige un chapitre pour les captures.
- Photo du premier écran : « Autumn Joy » par Memotions (https://www.flickr.com/photos/77994098@N00/291632767),
  licence CC BY 2.0, recadrée et compressée ; crédit en pied de page.
- Photo de la page Contact : « courtyard » par Serge Melki (https://www.flickr.com/photos/67958110@N00/4708186264),
  licence CC BY 2.0.
- Polices Gloock, Hanken Grotesk, DM Mono (SIL OFL), Three.js et Lenis (MIT) : voir `licenses/`.

Les sources (plans, calendrier, outils de capture) sont dans l’atelier de M&S Design ;
ce dépôt est la copie publiée, exportée par `_msdesign-src/strate/export.mjs`.
