# Identité Tabtree

Le signe est un **« T » construit avec le vocabulaire du produit** : trois nœuds reliés par des
connecteurs, exactement les éléments d'une carte Tabtree. Il dit l'initiale de la marque et la
structure arborescente dans une seule forme. Posé sur un capuchon de touche, il devient l'icône
d'application et rappelle la promesse du nom : `Tab` crée une branche.

## Fichiers

| Fichier | Usage |
|---|---|
| `tabtree-mark.svg` | Le signe seul, tracé en `currentColor`. C'est la version à inliner. |
| `tabtree-icon.svg` | Icône d'app : signe sur capuchon de touche, coins arrondis. Favicon, onglets, raccourcis. |
| `tabtree-icon-maskable.svg` | Plein cadre, sans coins arrondis. Stores et icônes PWA `maskable` : l'OS applique son propre masque. |
| `tabtree-lockup.svg` / `-dark.svg` | Signature horizontale (signe + mot), pour fond clair / fond sombre. |
| `tabtree-icon-512.png`, `-192.png` | Rendus PNG de l'icône plein cadre (manifeste PWA). |
| `apple-touch-icon.png` | 180 × 180, écran d'accueil iOS. |
| `tabtree-lockup.png` / `-dark.png` | Signature en PNG 2× (README, réseaux sociaux, e-mails). |

L'icône est également **inlinée en data-URI dans `index.html`** comme favicon : l'app reste un
fichier unique, sans dépendance externe.

## Couleurs

| Rôle | Fond clair | Fond sombre |
|---|---|---|
| Accent (signe, « tree ») | `#3b82f6` | `#6ea8ff` |
| Encre (« Tab ») | `#1c2230` | `#e8ebf2` |
| Tranche du capuchon | `#2563c9` | `#4a86dd` |

Ce sont les variables `--accent` et `--ink` déjà définies dans l'app : l'identité et l'interface
partagent la même palette, elles ne peuvent pas diverger.

## Règles d'usage

- **Taille minimale** : 16 px pour l'icône, 20 px pour le signe seul. En dessous, les nœuds se
  referment sur les connecteurs et la forme devient une tache.
- **Zone de protection** : au moins la hauteur d'un nœud (⅛ de la largeur du signe) sur les
  quatre côtés.
- **Sur fond coloré ou photo** : utiliser l'icône sur capuchon, jamais le signe nu — il a besoin
  d'un fond calme pour tenir.
- **Ne pas** : changer les proportions, ajouter un contour, incliner la forme, remplir les nœuds
  d'une autre couleur que celle des connecteurs, ni recomposer le mot dans une autre graisse que
  800.

## Une réserve sur les signatures SVG

`tabtree-lockup.svg` et sa variante sombre rendent le mot avec un `<text>` reposant sur la pile de
polices système. C'est volontaire — le mot s'affiche alors dans la même police que l'interface —
mais cela signifie que **le rendu varie d'une plateforme à l'autre** et qu'il sera faux dans un
outil sans accès aux polices système. Pour de l'impression, un logiciel de PAO ou tout contexte où
le rendu doit être garanti au pixel près, vectoriser le texte au préalable, ou utiliser les PNG
fournis.
