# Rooted

La plateforme francophone pour apprendre le hacking éthique depuis son téléphone : un parcours de 30 jours, des machines à rooter et des défis CTF, dans le navigateur.

*Rooted* est un nom de travail. Il dit deux choses : obtenir les droits **root** sur une machine, c'est le but de chaque exercice ; être **bien enraciné**, c'est la promesse faite à l'apprenant. Si le nom change, seuls le logo et ce paragraphe changent : le reste de la charte reste valable.

## 1. Positionnement

- **Pour qui** : des débutants complets, souvent sur un Android d'entrée de gamme, avec des données mobiles limitées. Beaucoup n'ont pas d'ordinateur.
- **Ce qu'on promet** : progresser un peu chaque jour, pratiquer sur de vraies commandes, comprendre comment corriger chaque faille.
- **Ce qu'on refuse** : le cliché du hacker à capuche, la culture de l'intrusion illégale, l'effet « film ». Rooted forme des défenseurs.

Trois mots résument la personnalité de la marque : **précis, rassurant, légal**.

## 2. Ton et écriture

On parle comme un grand frère qui connaît le métier : direct, chaleureux, jamais condescendant.

| Règle | Oui | Non |
|---|---|---|
| Tutoyer | « Valide sur ton téléphone » | « Veuillez valider… » |
| Phrases courtes, verbe d'action | « Continuer la mission » | « Cliquez ici pour poursuivre votre progression » |
| Expliquer le jargon la première fois | « IDOR : voir les données d'un autre en changeant un numéro » | « Exploite l'IDOR » |
| Dire ce qui se passe | Bouton « Payer 5 000 FCFA » puis « Paiement reçu » | Bouton « OK » |
| Erreurs utiles, sans excuses | « Ce n'est pas le bon drapeau pour root.txt. Vérifie l'orthographe. » | « Oups ! Une erreur est survenue » |
| Toujours rappeler le cadre | « Cible autorisée : 10.10.0.11 » | « Pirate ce serveur » |

Les commandes, adresses IP, chemins et drapeaux s'écrivent toujours en police mono : `nmap -sV`, `10.10.0.11`, `flag{…}`. Les montants s'écrivent avec une espace : **5 000 FCFA**.

## 3. Logo

Le logo est un mot-symbole tracé en monoline sur une grille de 8 px : les lettres `rooted` suivies d'un **curseur de terminal ambre**. Le curseur est la signature de la marque : il signifie « à toi de taper ».

| Fichier | Usage |
|---|---|
| `rooted-wordmark-sur-sombre.svg` | Sur `bg`, `surface` ou toute photo sombre. |
| `rooted-wordmark-sur-clair.svg` | Sur fond blanc ou `bg` du thème clair. |
| `rooted-icone.svg` | Icône d'appli, favicon, avatar de réseaux sociaux. Le `r` et le curseur seuls. |

- **Zone de protection** : autour du logo, laisser au moins la hauteur du curseur (48 unités de la grille, soit ~60 % de la hauteur du logo).
- **Taille minimale** : 96 px de large pour le mot-symbole, 24 px pour l'icône.
- **Le curseur reste ambre** (`brand`), sur tous les fonds. Dans l'interface, il peut clignoter (1 s, 50 % allumé) ; sur un support imprimé, il est fixe.
- **À ne pas faire** : changer la couleur des lettres en ambre, déformer, ajouter une ombre ou un dégradé, mettre le curseur avant le mot, l'écrire dans une autre police.

## 4. Couleurs

Rooted est **sombre par défaut** : c'est l'univers du terminal, et c'est plus économe en batterie sur les écrans OLED. Un thème clair existe pour la lecture longue et l'impression.

- **Ambre (`brand`) = l'action.** Une seule action principale par écran porte l'ambre. Il sert aussi au curseur du logo, à l'étape en cours et à l'invite du terminal. Il n'est jamais décoratif.
- **Vert (`success`) = c'est acquis** : drapeau trouvé, étape faite, machine en ligne.
- **Rouge (`danger`) = erreur**, toujours avec un texte qui dit quoi faire.
- **Bleu (`focus`) = navigation au clavier**, uniquement pour l'anneau de focus.
- **Texte ambre sur fond clair** : toujours `brand-text`, jamais `brand` (contraste insuffisant).
- **Le terminal reste sombre** dans les deux thèmes (`term-bg`, `term-ink`, `term-prompt`).

Répartition visée sur un écran : ~80 % de neutres (`bg`, `surface`, `line`), ~15 % de texte, ~5 % d'ambre.

## 5. Typographie

Trois familles Google Fonts, gratuites et légères :

- **Chakra Petch** (`display`) : titres seulement. Ses angles coupés évoquent l'électronique sans tomber dans le pastiche.
- **IBM Plex Sans** (`sans`) : tout le texte courant et les boutons. Très lisible en petit.
- **IBM Plex Mono** (`mono`) : commandes, adresses, points, sur-titres en capitales.

Règles : 16 px minimum dans les champs de saisie (évite le zoom automatique sur mobile) ; pas plus de deux tailles de titre par écran ; les sur-titres (`eyebrow`) sont en capitales espacées et toujours en `ink-muted` ou `brand-text`. Charger seulement les graisses utilisées (Chakra 600, Plex Sans 400/500/600, Plex Mono 400/500/600) et activer le mode léger, qui retombe sur les polices système.

## 6. Mise en page

- **Mobile d'abord** : une colonne, marges latérales `space-5` (20 px), jamais moins de `space-4`.
- **Une action principale par écran**, en bas de l'écran, à portée de pouce, hauteur `button-h`.
- **Navigation** : quatre onglets en bas (Accueil, Parcours, Labo, Profil). Dans une machine, on cache les onglets : mode concentration.
- **Cibles tactiles** : `tap-min` (44 px) minimum.
- **Cartes** : `surface` + bordure `line` + `radius-lg`. Pas d'ombre portée. La carte principale d'un écran peut prendre `radius-xl`.
- **Page web** : conteneur de 1 180 px, sections séparées par une bordure `line` et l'alternance `bg` / `nav`.

## 7. Iconographie

Icônes au trait de 2 px, extrémités arrondies, sur une grille de 24 px, dans la couleur du texte qui les accompagne. Formes simples : maison, chemin, terminal (`>_`), drapeau, ampoule (indice), cadenas, profil. Pas d'icônes pleines, pas d'emoji, pas de têtes de mort ni de capuches.

## 8. Formes et motifs

Le motif de la marque est une **grille de points** au pas de `space-4`, rappel du quadrillage d'un écran de terminal, avec des blocs pleins taillés dans les rayons du système et le curseur ambre comme ponctuation. On l'utilise sur les couvertures, les visuels de réseaux sociaux et les certificats, jamais derrière du texte courant.

## 9. Mouvement

- Transitions d'interface : 150 ms, `ease-out`. Rien de plus long sauf l'apparition d'une feuille (220 ms).
- Le curseur clignote à 1 s. Une sortie de terminal peut s'afficher ligne par ligne, 20 ms par ligne, pour l'effet « commande en cours ».
- Une seule célébration : quand une machine est rootée (le curseur se transforme en coche). Pas de confettis.
- Respecter `prefers-reduced-motion` : plus de clignotement, plus d'animation de sortie.

## 10. Accessibilité

- Contraste 4.5:1 pour tout texte, 3:1 pour les bordures de contrôle, les icônes et l'anneau de focus, dans les deux thèmes (vérifié pour chaque paire de jetons ci-dessus).
- Un état ne se lit jamais par la couleur seule : coche, mot ou icône en plus.
- Anneau de focus `focus`, 2 px, décalé de 2 px.
- Le terminal propose des touches à l'écran (Tab, ↑, Ctrl+C) et un réglage de taille de texte.

## 11. Applications

- **Visuel réseaux sociaux** (1 080 × 1 080) : fond `bg`, grille de points, un titre en Chakra Petch, une commande en mono, le mot-symbole en bas à gauche.
- **Certificat de fin de parcours** (A4 paysage, thème clair) : mot-symbole, nom de l'apprenant en `display-lg`, liste des machines rootées en mono.
- **Paiement mobile money** : les noms des portefeuilles (Orange Money, Moov Money, Wave, NanaPay) et des passerelles (LigdiCash, CinetPay) s'écrivent en texte, dans notre typographie. On n'affiche leurs logos officiels qu'en respectant leur propre charte, si leur contrat l'autorise.
- **Rappel légal** : toute communication qui montre une attaque précise que la cible est un labo autorisé.
