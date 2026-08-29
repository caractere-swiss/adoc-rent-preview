# Visuels web RENT — repli de catégorie + photos de parc

Produit par le chat Web (adoc-assainissement-volleges), 28.08.2026.
Destination : dépôt `caractere-swiss/adoc-rent`, `assets/` — le dépôt Git est le
SEUL canal de transfert mesuré comme fonctionnel vers Claude Code.

## pictos/ — 11 pictogrammes de service, repli de CATÉGORIE

Source : `_ressources/pictos/*.jpg`, originaux ADOC, dessin au trait noir sur
blanc, 2534 à 2683 px de côté, circulaires.

Méthode : niveaux de gris → négatif → `-level 8%,92%` pour durcir le seuil →
le résultat sert de canal ALPHA sur un aplat uni `#F2F5F7` (couleur de texte de
la charte, cf. DESIGN.md §4.2) → détourage `-trim` → recadrage CARRÉ centré sur
fond transparent → WebP q88 en 512 et 1024 px.

Contrôle visuel FAIT : planche des 11 pictos en 512 px composités sur `#0D1418`,
lus à l'écran. Trait blanc net, cercles complets, aucun résidu de fond blanc,
cadrages homogènes.

Poids : 196 Ko pour les 11 en 512 px (13 à 23 Ko pièce) · 376 Ko en 1024 px.

⚠️ **Ils illustrent un SERVICE, jamais une machine précise.** Emploi autorisé :
repli de fiche matériel SANS photo, à l'échelle de la CATÉGORIE. Interdit : les
présenter comme la photo du matériel, ou les faire porter la mention
« photos non contractuelles » — ce ne sont pas des photos.

Correspondance des 11 fichiers avec les catégories du site : À ÉTABLIR par
Claude Code contre le mapping existant des mascottes (`inc/mascottes.php`).
Ces pictos ne remplacent pas les mascottes de catégorie — ils comblent la fiche
matériel, un cran plus bas.

## photos/ — 4 photos RÉELLES du parc, aucun droit à demander

| Fichier | Sujet | Source |
|---|---|---|
| `volvo-fm330-hydrocureur-flanc-gauche` | Volvo FM330, flanc gauche | ADOC (`VS13288-gauche.jpeg`, 1600x1200) |
| `volvo-fm330-hydrocureur-face` | Volvo FM330, face | ADOC (`VS13288-face.jpeg`, 1200x1600) |
| `man-tgs-35510-aspirateur-1` et `-2` | MAN TGS 35.510 aspirateur | ADOC, reçues le 24.07 (2048x1536) |

WebP q82, largeurs 800 et 1600, EXIF retiré, orientation appliquée.
⚠️ Volvo FM330 : le côté DROIT manque toujours.
⚠️ Ces quatre-là sont des photos de matériel : la mention « photos non
contractuelles » s'applique, elle est déjà automatique côté code.

## Ce que ce lot ne contient PAS

`ADOC_catalogue_prestations.pdf` (28 pages, 26,5 Mo) porte **88 JPEG de plus de
15 Ko — photos réelles du parc ADOC** : super aspirateurs, camion grue Multilift,
balayeuses, Scania et MAN bennes, pick-up, camionnettes d'inspection et leurs
régies, robots de fraisage, caméras. Inventoriées à l'œil, non encore extraites :
le fichier déposé sur le kDrive est un placeholder cloud non matérialisé
(27 745 853 octets, tous nuls — mesuré des deux côtés, `device_bash` et stage,
md5 `68f9582b9cbcdf031a5ded3963457dd9`). À reprendre dès matérialisation.

Fait négatif mesuré, à ne pas rouvrir : `Catalogue_Loc_sans_prix_OK.pdf`
(12 pages, rastérisé à **150 dpi**) ne contient **aucune photo de machine** —
tableaux de prix vides, mascottes ADOC en bandeau, deux pictos avant/après.
