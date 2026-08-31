# Polices locales (RGPD)

Aucune police externe (pas de Google Fonts distant). Les fichiers `.woff2` sont
servis **localement** depuis ce dossier.

## Typographie arrêtée (24.08.2026, chantier A1)

**Archivo** (texte courant) + **Archivo Expanded** (titres), licence
[SIL Open Font License 1.1](https://openfontlicense.org). Sous-ensembles latin
+ latin-étendu uniquement. Fichiers présents :

- `principale.woff2` / `principale-latin-ext.woff2` — Archivo, graisse 400
- `principale-medium.woff2` / `principale-medium-latin-ext.woff2` — Archivo, graisse 500
- `titres-semibold.woff2` / `titres-semibold-latin-ext.woff2` — Archivo Expanded, graisse 600
- `titres-bold.woff2` / `titres-bold-latin-ext.woff2` — Archivo Expanded, graisse 700

« Archivo Expanded » n'est plus distribuée comme famille séparée dans la fonte
variable Archivo actuelle : les fichiers `titres-*` sont des instances
statiques figées à l'axe de largeur `wdth=125` (« Expanded ») — mêmes contours
sources, aucune modification, simplement un cliché statique de cet axe pour un
chargement `@font-face` classique par graisse (comme `principale-*`).

Origine : instances statiques générées par l'API CSS de Google Fonts (mêmes
fichiers `.woff2` que la distribution officielle OFL, seule la méthode de
récupération diffère), puis auto-hébergées ici — **aucun appel à Google au
chargement du site**, conformément à la contrainte RGPD posée dès la v0.1.

Déclarations `@font-face` : voir `assets/scss/base/_fonts.scss`.

> Le repli système (`system-ui, -apple-system, Segoe UI, Roboto, Arial,
> sans-serif`) reste actif dans `$police-principale`/`$police-titres`
> (`_tokens.scss`) : si un fichier venait à manquer, le texte reste lisible.
