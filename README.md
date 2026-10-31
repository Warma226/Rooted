# Rooted

Plateforme francophone pour apprendre le **hacking éthique** depuis son téléphone : un parcours de 30 jours, des machines simulées à rooter et des défis CTF, directement dans le navigateur.

> Tout le labo est **simulé dans le navigateur** : aucune vraie machine n'est attaquée. Ailleurs, tester un système sans l'accord écrit de son propriétaire est illégal.

## Ce qu'il y a dans ce dépôt

| Chemin | Contenu |
|---|---|
| `index.html` | Page d'accueil : présentation, fonctionnement, labo, tarif, règles |
| `app.html` | L'application : Parcours (30 jours), Labo (3 machines + 12 défis CTF), Quiz, Mémo |
| `assets/logos/` | Mot-symbole (fond sombre, fond clair) et icône d'appli en SVG |
| `assets/brand/tokens.json` | Jetons de la charte : couleurs (sombre / clair), typographie, espacements, arrondis |
| `docs/charte-graphique.md` | La charte graphique complète (logo, couleurs, typo, voix, composants) |
| `docs/*.pdf` | Le programme de 30 jours et le cours de 100 pages |

Le site est **100 % statique** : du HTML, du CSS et du JavaScript, sans serveur ni installation. La progression de chaque apprenant est enregistrée dans son navigateur (`localStorage`).

## Mettre le site en ligne avec GitHub Pages

Faisable depuis un téléphone :

1. Sur GitHub, ouvre le dépôt **Warma226/Rooted** → **Settings** → **Pages**.
2. Dans **Source**, choisis **Deploy from a branch**, puis la branche **main** et le dossier **/ (root)**. Enregistre.
3. Après une ou deux minutes, le site est en ligne à l'adresse `https://warma226.github.io/Rooted/`.

## Tester en local (avec un ordinateur)

Ouvre `index.html` dans un navigateur, ou lance un petit serveur :

```bash
python3 -m http.server 8000
# puis http://localhost:8000
```

## Le labo

| Machine | Niveau | Notions |
|---|---|---|
| Boulangerie | Facile | Scan, code source, secrets en clair, réutilisation de mot de passe |
| Archives | Facile+ | FTP anonyme, hachage sans sel, programme SUID |
| Portail | Moyen | IDOR, injection SQL |

Le terminal simulé comprend `nmap`, `curl`, `ssh`, `ftp`, `ls`, `cat`, `cd`, `find`, `sudo -l`, `su`, `grep`, `base64`, `rot13`, `xxd` et `hashcheck`, avec les pipes `|`. Chaque machine a deux drapeaux (user et root), des indices progressifs et un débrief sur la correction.

## Feuille de route

- [ ] **Comptes utilisateurs** et synchronisation de la progression entre appareils (nécessite un backend).
- [ ] **Abonnement Membre à 5 000 FCFA / mois** par mobile money (Orange Money, Moov Money, Wave, NanaPay) via LigdiCash ou CinetPay. Le paiement doit être validé **côté serveur** par la notification de la passerelle ; ne jamais débloquer l'accès depuis le navigateur seul. Vérifier les portefeuilles acceptés et les frais auprès de chaque passerelle.
- [ ] Nouvelles machines (Windows, Wi-Fi) et nouveaux défis.
- [ ] Mode léger (polices système, aucune ressource externe) pour économiser les données.
- [ ] Choix définitif du nom et dépôt de la marque.

## Charte graphique en bref

- Thème **sombre par défaut**, thème clair disponible.
- **Ambre `#FFB020`** réservé à l'action principale (une seule par écran) et au curseur du logo.
- Polices Google Fonts : **Chakra Petch** (titres), **IBM Plex Sans** (texte), **IBM Plex Mono** (commandes).
- Ton : tutoiement, phrases courtes, jargon expliqué, cadre légal toujours rappelé.

Détails dans [`docs/charte-graphique.md`](docs/charte-graphique.md).
