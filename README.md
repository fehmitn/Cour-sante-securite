# 🛡️ Vigilance SST

### Serious game **Santé & Sécurité au Travail** — 3 niveaux, mode examen, 570 points de vigilance, 100 % hors-ligne

<p>
  <img alt="HTML5" src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white">
  <img alt="CSS3" src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white">
  <img alt="JavaScript" src="https://img.shields.io/badge/JavaScript_vanilla-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black">
  <img alt="SVG ISO 7010" src="https://img.shields.io/badge/SVG-ISO_7010-ffb000?style=for-the-badge&logo=svg&logoColor=black">
</p>
<p>
  <img alt="Hors-ligne" src="https://img.shields.io/badge/100%25_hors--ligne-1c9c63?style=flat-square">
  <img alt="Zéro dépendance" src="https://img.shields.io/badge/z%C3%A9ro_d%C3%A9pendance-0ea5a4?style=flat-square">
  <img alt="Sauvegarde locale" src="https://img.shields.io/badge/progression-localStorage-1466d8?style=flat-square">
  <img alt="Dépôt" src="https://img.shields.io/badge/GitHub-Cour--sante--securite-181717?style=flat-square&logo=github&logoColor=white">
  <img alt="Licence MIT" src="https://img.shields.io/badge/licence-MIT-2ea44f?style=flat-square">
</p>

> **Vigilance SST** est une application web de gamification qui transforme les règles de santé et de
> sécurité au travail en un parcours ludique : un quiz sur les fondamentaux, des scénarios
> d'équipement EPI, un jeu de reconnaissance des signaux ISO 7010 et un **mode examen imprimable**.
>
> Un seul fichier, aucun serveur, aucune installation : **double-cliquez, jouez, progressez.**
>
> 📴 **L'application fonctionne entièrement hors-ligne** : une fois `index.html` téléchargé, elle
> s'exécute sans connexion Internet, sans serveur et sans aucune dépendance externe. Les seules
> ressources réseau de ce dépôt sont les **badges** ci-dessus, purement décoratifs — le jeu, lui,
> n'effectue aucune requête. La seule URL embarquée volontairement est celle du **déchiffreur du
> corrigé** (`decode.html`, hébergé sur GitHub Pages) encodée dans les QR du mode examen.

### 📴 Mode hors-ligne natif

`index.html` est un fichier **autonome** : HTML, CSS, JavaScript et pictogrammes SVG sont embarqués
dans le même document. Aucun CDN, aucune police distante, aucun appel réseau au chargement ni
pendant le jeu. Il suffit du fichier sur une clé USB pour animer une session de sensibilisation en
salle, sur un poste isolé ou sans Wi-Fi. La progression reste sur l'appareil (`localStorage`).

---

## 📑 Sommaire

- [🎯 Le projet](#-le-projet)
- [✨ Fonctionnalités](#-fonctionnalités)
- [🎮 Le parcours en 3 niveaux](#-le-parcours-en-3-niveaux)
- [🖨️ Mode examen](#-mode-examen)
- [🔓 QR du corrigé chiffrés par PIN](#-qr-du-corrigé-chiffrés-par-pin)
- [🏅 Score, rangs et badges](#-score-rangs-et-badges)
- [🧱 Technologies utilisées](#-technologies-utilisées)
- [📁 Arborescence](#-arborescence)
- [🚀 Lancer le jeu](#-lancer-le-jeu)
- [📚 Contenu pédagogique et sources](#-contenu-pédagogique-et-sources)
- [♿ Accessibilité et qualité](#-accessibilité-et-qualité)
- [🤝 Contribution](#-contribution)
- [📄 Licence et crédits](#-licence-et-crédits)

---

## 🎯 Le projet

Les formations SST sont souvent descendantes : un support, des slides, un questionnaire papier.
**Vigilance SST** propose l'inverse — un mini-jeu navigable qui fait *manipuler* les notions clés :

| Objectif | Réponse apportée |
| :-- | :-- |
| Ancrer les définitions (accident, maladie professionnelle, feu, EPI) | 🔍 Quiz de 10 questions tirées d'une banque de 25, avec explication systématique |
| Faire le lien entre risque et protection | 🧰 4 situations de travail à équiper correctement |
| Reconnaître les familles de signaux d'un coup d'œil | ⚡ Flash de 12 s sur 20 pictogrammes ISO 7010 |
| Évaluer les acquis sur papier | 🖨️ Examen A4 de 10 questions, 3 scénarios EPI et 10 signaux, corrigé optionnel |
| Donner envie de rejouer | 🏆 570 PV, 5 rangs, 5 badges, meilleurs scores conservés et tirage aléatoire |
| Rester utilisable en salle, sans réseau | 📴 Fichier local, aucune dépendance externe |

Public visé : nouveaux arrivants, sensibilisation annuelle, ateliers de prévention, étudiants en
hygiène-sécurité, formateurs cherchant un support d'ouverture ou de révision.

---

## ✨ Fonctionnalités

- 🧭 **Tableau de bord unifié** — score global, anneau de progression, rang courant et état des 3 niveaux.
- 🎯 **Parcours progressif** — les niveaux s'enchaînent, mais restent accessibles librement (navigation par onglets).
- 🎲 **Quiz aléatoire** — 10 questions tirées parmi 25 à chaque tentative (dont au moins 2 de manutention), sans reprendre exactement la même sélection.
- 💾 **Progression persistante** — meilleurs scores sauvegardés dans `localStorage` (clé `vigilance_sst_v1`), appareil par appareil.
- 🔁 **Rejouabilité** — chaque tentative peut améliorer le record ; le score total ne régresse jamais.
- 🧾 **Feedback pédagogique** — chaque réponse est expliquée (bonne ou mauvaise), sans jamais laisser l'apprenant deviner.
- ⏱️ **Chrono temps réel** — niveau 3, 12 secondes par signal, barre qui passe en alerte à 4 s.
- 🏅 **Rangs et badges** — 5 paliers de « Observateur » à « Légende SST » et 5 badges de réussite.
- 🧰 **Visuel EPI interactif** — un travailleur SVG réagit aux équipements sélectionnés, protections auditives comprises.
- 🧯 **Pictogrammes officiels** — 20 signaux ISO 7010 intégrés en SVG inline, sans chargement réseau.
- 📱 **Responsive** — grilles fluides du mobile au grand écran, barre supérieure collante.
- ♿ **Accessible** — HTML sémantique, `aria-live` sur les retours, `aria-modal`, focus visibles, `prefers-reduced-motion`.
- 🖨️ **Mémo en 3 sous-pages** — pages 1–6 (fondamentaux), pages 8–16 (notions de sécurité) et onglet équipements : EPI, familles de signaux et pictogrammes de manutention normalisés en SVG.
- 🧾 **Mode examen** — 10 questions du niveau 1 (dont au moins 2 de manutention), 3 scénarios EPI et 10 signaux tirés au hasard, document A4 avec corrigé optionnel sur une page séparée.
- 🔗 **Routes par ancre** — `#dashboard`, `#quiz`, `#ppe`, `#signals`, `#exam`, `#memo` : chaque écran est partageable.

---

## 🎮 Le parcours en 3 niveaux

| # | Niveau | Mécanique | Contenu | Barème |
| :-: | :-- | :-- | :-- | :-- |
| **01** | 🔍 **Les fondamentaux** | Quiz à choix unique, correction expliquée | Banque de 25 questions, 10 tirées au hasard par session (≥ 2 de manutention) | 10 PV / bonne réponse → **100 PV par session** (250 PV banque complète) |
| **02** | 🧰 **Bien s'équiper** | Sélection multiple d'EPI sur 4 situations | Chantier extérieur · Travail en hauteur · Laboratoire · Atelier de meulage | 10 PV / EPI correct, −5 PV / EPI inutile → **120 PV** |
| **03** | ⚡ **L'œil du safety** | Reconnaissance de famille sous contrainte de temps | 20 pictogrammes, 5 familles ISO 7010 | 10 PV / signal en moins de 12 s → **200 PV** |
| | | | **Total** | **570 PV** |

### 01 · 🔍 Quiz SST — « Les fondamentaux »

- **25 questions en banque**, dont **10 tirées au hasard** à chaque session avec un minimum garanti de **2 questions de manutention** (pictogrammes de colis, techniques de levage) : deux parties ne proposent pas le même parcours.
- Une seule bonne réponse, validation puis correction immédiate.
- Chaque question est accompagnée d'une **explication courte** issue du support de formation.
- Panneau latéral : les 25 questions de la banque avec ✓ pour celles déjà maîtrisées ; la maîtrise est conservée d'une session à l'autre.
- Écran de fin : bonnes réponses sur 10, meilleur score global sur 250, message adapté (≥ 80 %, ≥ 50 %, sinon révision du mémo).

### 02 · 🧰 Équipez le travailleur

Quatre scénarios, trois risques, trois EPI indispensables à chaque fois :

| Scénario | Risques | EPI attendus |
| :-- | :-- | :-- |
| 🏗️ **Chantier extérieur** — déchargement de palettes | Chute d'objets, coupures, écrasement des pieds | Casque, gants, chaussures de sécurité |
| 🪜 **Travail en hauteur** — contrôle sur échafaudage | Chute de hauteur, chute d'outils, perte d'équilibre | Casque, chaussures de sécurité, harnais antichute |
| 🧪 **Laboratoire** — manipulation de produit chimique | Projections, contact cutané, vapeurs irritantes | Gants chimiques, lunettes, masque respiratoire |
| ⚙️ **Atelier de meulage** — meulage d'une pièce métallique | Projections oculaires, bruit intense, coupures aux mains | Lunettes, gants, protections auditives |

Le calcul est volontairement nuancé : **+10 PV** par EPI attendu, **−5 PV** par EPI superflu,
score borné entre 0 et 30 par scénario. Le meilleur résultat est conservé.

### 03 · ⚡ Reconnaissance des signaux

Vingt pictogrammes, cinq familles, douze secondes. La réponse est un clic sur la famille perçue :

| Famille | Forme et couleur | Exemples |
| :-- | :-- | :-- |
| 🔵 **Obligation** | Rond bleu, inscription blanche | Casque · Lunettes · Gants · Protection auditive |
| 🔴 **Interdiction** | Rond blanc, contour rouge, cercle barré | Fumer · Téléphone · Flamme nue · Ne pas toucher |
| 🟡 **Danger** | Triangle jaune, inscription noire | Électrique · Incendie · Danger général · Matières toxiques |
| 🟢 **Secours** | Carré vert, inscription blanche | Premiers secours · Civière · Rassemblement · Rince-œil |
| 🧯 **Incendie** | Carré rouge, inscription blanche | Extincteur · Boyau d'incendie · Échelle · Point d'alarme |

À l'expiration du chrono, la réponse est comptée fausse — mais le pictogramme et sa famille sont
toujours expliqués, pour transformer l'erreur en apprentissage.

---

## 🖨️ Mode examen

Le mode examen transforme la banque de contenus en une **épreuve papier prête à imprimer**, sans
quitter l'application et sans connexion réseau.

| Partie | Tirage | Barème indicatif |
| :-- | :-- | :-: |
| Niveau 1 · fondamentaux | 10 questions tirées parmi 25, dont au moins 2 de manutention, 4 choix par question, 4 pts par bonne réponse | 40 pts |
| Niveau 2 · EPI | 3 scénarios tirés parmi 4, 3 EPI à cocher par scénario, 10 pts par scénario correct | 30 pts |
| Niveau 3 · signaux | 10 pictogrammes tirés parmi 20, 1 famille à cocher, 3 pts par bonne famille | 30 pts |
| | **Total** | **100 pts** |

- **Tirage aléatoire sans répétition** à l'intérieur de chaque partie, avec un code de sujet
  (`EX-AAAAMMJJ-NN`) et une date de génération.
- Document **A4** avec en-tête, champs nom/prénom/date, consignes, cases à cocher et barème.
- **Corrigé optionnel** : la case « Inclure le corrigé » ajoute une page séparée, détachable avant
  distribution.
- **QR corrigé chiffrés par PIN** : quand le corrigé est activé, trois QR code sont imprimés dans le
  sujet lui-même (un par page). Qui scannent un QR arrivent sur le déchiffreur en ligne —
  **[fehmitn.github.io/Cour-sante-securite/decode.html](https://fehmitn.github.io/Cour-sante-securite/decode.html)** —
  avec le corrigé **chiffré** dans l'URL : la page des réponses n'est pas accessible sans le PIN.
  Voir [🔓 QR du corrigé](#-qr-du-corrigé-chiffrés-par-pin) ci-dessous.
- Impression par le bouton **Imprimer** ou par `Ctrl+P` / `Cmd+P` ; seule l'épreuve est imprimée,
  sans la navigation de l'application.
- **3 pages fixes** : page 1 = entête + partie 1, page 2 = suite de la partie 1 + partie 2
  (scénarios 1 et 2), page 3 = entête institutionnelle répétée en haut, scénario 3 de la partie 2
  puis partie 3.
- **Lisible en noir & blanc** : dans la partie 3, la couleur de chaque pictogramme est indiquée
  entre parenthèses — ex. « (Couleur : jaune) » — avant la ligne de réponses A–E ; les panneaux
  d'interdiction précisent « (Couleur : cercle et barre rouge) ».
- **Accès protégé par déverrouillage** : le mode examen demande un mot de passe (modale dédiée).
  La vérification ne stocke jamais le mot de passe en clair : quatre tableaux de nombres à quatre
  chiffres, générés aléatoirement, encodent un chiffre attendu par rang (le rang 0 des éléments de
  `TAB1`, le rang 1 de `TAB2`, etc.) et le code compare chaque chiffre saisi aux éléments des
  tableaux du rang correspondant. Protection simple, adaptée à un usage en classe.
  **Le mot de passe n'est pas partagé ici : demandez-le au créateur du fichier**
  (Fehmi Ben Njima — fehmitn@gmail.com).
- Le mode examen est **indépendant de la progression** : il ne modifie ni les scores, ni les badges,
  ni les meilleurs résultats.
- Astuce : choisir « Enregistrer au format PDF » dans la boîte d'impression pour archiver un sujet.

Accès direct : `index.html#exam`.

---

## 🔓 QR du corrigé chiffrés par PIN

Quand « Inclure le corrigé » est cochée, deux protections empêchent les apprenants d'accéder aux
réponses : le mot de passe du mode examen côté formateur, et un **code PIN** côté sujet imprimé.

### Comment ça marche

| Étape | Où | Ce qui se passe |
| :-: | :-- | :-- |
| 1 | `index.html` | Au clic sur **Imprimer** (corrigé activé), une modale demande un **PIN numérique de 4 à 8 chiffres**. Il n'est **jamais stocké** : il sert uniquement à dériver la clé de chiffrement. |
| 2 | Sujet imprimé | Chacune des **3 pages** du sujet porte un **QR code** encodant une URL du déchiffreur avec le corrigé de la page **chiffré** : `https://fehmitn.github.io/Cour-sante-securite/decode.html?text=SST1…` |
| 3 | Puzzle papier | Les réponses sont réparties : page 1 = questions 1–6 · page 2 = questions 7–10 + scénarios 1–2 · page 3 = scénario 3 + familles des signaux. Il faut donc les **trois pages** pour disposer du corrigé complet. |
| 4 | `decode.html` | Le scanneur ouvre l'URL (pré-remplie). Il saisit le **PIN choisi par le formateur** : le corrigé s'affiche, déchiffré **100 % localement** dans le navigateur. |
| 5 | Mauvais PIN | Le déchiffreur affiche « PIN incorrect ou contenu illisible » — **jamais** le corrigé, même partiellement. |

### Chiffrement (fait maison, sans dépendance)

- Clé = **SHA-256** du PIN (implémentation SHA-256 écrite à la main, ~64 constantes, aucune API
  navigateur requise).
- Chiffrement par **XOR en flux** : chaque bloc de 32 octets est masqué par le condensé SHA-256 de
  `sst-qr|clé|numéro-de-bloc`.
- Un **checksum FNV-16** est préfixé au texte clair : un mauvais PIN donne un contrôle échoué, donc
  une erreur — jamais de corrigé aléatoire.
- Le tout est encodé en **Base32** (alphabet sans `+` ni `=`, sûr dans une URL) avec le préfixe `SST1`.

Le fichier `decode.html` du dépôt **est** le déchiffreur : autonome (~12 Ko, aucune dépendance), il
fonctionne aussi localement en `file://`, et depuis GitHub Pages à l'adresse
<https://fehmitn.github.io/Cour-sante-securite/decode.html>. La page dépend d'Internet uniquement
parce que le QR encode une URL en ligne — le chiffrement, lui, reste 100 % local.

> 🔐 **Limites honnêtes** : ce chiffrement protège un corrigé papier contre la curiosité immédiate.
> Ce n'est pas du chiffrement certifié (pas d'AES, pas de HMAC) ; un PIN numérique de 4 chiffres
> reste trouvables par force brute si quelqu'un recopie le contenu du QR. Choisissez un PIN de
> 6 à 8 chiffres pour un cours sérieux.

---

## 🏅 Score, rangs et badges

**Points de Vigilance (PV)** : 570 au maximum, affichés en permanence dans la barre supérieure et le pied de page.

| Rang | Seuil | Message |
| :-- | :-: | :-- |
| 👀 Observateur | 0 PV | Le point de départ de toute vigilance |
| 🟢 Vigilant | 110 PV | Les réflexes commencent à s'installer |
| 🛡️ Gardien SST | 270 PV | Vous savez reconnaître et prévenir |
| 🎓 Expert SST | 420 PV | Les fondamentaux sont solides |
| 🏆 Légende SST | 570 PV | Parcours complet, sans faute |

Badges débloqués en cours de route : **Premier pas** · **Quiz terminé** · **Bien équipé** ·
**Œil de lynx** · **Légende SST**.

La réinitialisation (icône ↻) efface scores et badges **uniquement sur l'appareil courant**,
après confirmation dans une boîte de dialogue accessible.

---

## 🧱 Technologies utilisées

| Brique | Usage |
| :-- | :-- |
| **HTML5 sémantique** | Structure `header`/`nav`/`main`/`section`/`footer`, landmarks ARIA, `lang="fr"`, meta description |
| **CSS3 pur** | Variables `:root`, CSS Grid, Flexbox, `clamp()`, dégradés radiaux, animations et media queries — *aucun framework CSS* |
| **JavaScript ES6+ (vanilla)** | État applicatif, routage par hash, rendu par templates, `localStorage`, timers — *aucune bibliothèque, aucun build* |
| **SHA-256 & chiffrement maison** | Vérification du mot de passe examen par rangs et chiffrement du corrigé QR (XOR par flux de condensés SHA-256, checksum FNV-16, Base32) — implémentation manuscrite, sans API Web Crypto ni bibliothèque |
| [**qrcode-generator 1.4.4**](https://www.npmjs.com/package/qrcode-generator) | Génération des QR codes du corrigé — *Copyright (c) 2009 Kazuhiko Arase*, licence **MIT**, bibliothèque minifiée (~24 Ko) et **embarquée inline** dans `index.html` |
| **SVG** | Pictogrammes **ISO 7010** aux `viewBox` variés (265×265, 600×525, 200×200, 100×100, 52,9×52,9), sprite `<symbol>` inline, travailleur et jauges animés, **logo de l'établissement** (`#csfmi-logo`, 1241×1241) |
| **localStorage** | Persistance `vigilance_sst_v1` : meilleurs scores, niveaux terminés, réinitialisation |

> 🧊 **Zéro dépendance, zéro requête réseau.** Pas de CDN, pas de police distante, pas de
> `npm install` : l'application est un `index.html` autonome (~305 Ko, avec la bibliothèque QR
> embarquée) et un `decode.html` autonome — les deux fonctionnent en `file://`.

---

## 📁 Arborescence

```text
Cour-sante-securite/
├── index.html                    # Application complète : HTML + CSS + JS + pictogrammes + logo + lib QR inline
├── decode.html                   # Déchiffreur autonome du corrigé QR (fonctionne aussi sur GitHub Pages)
├── logo.svg                      # Logo du centre (source, embarqué dans index.html)
├── README.md                     # Ce document
├── LICENSE                       # Licence MIT (code) + note sur les contenus et pictogrammes
└── sst.pdf                       # Support de formation M02 (source pédagogique)
```

Tous les pictogrammes sont **embarqués en SVG inline** dans `index.html` : le dépôt ne contient aucun
fichier SVG séparé. Aucun chargement de fichier externe n'est effectué, donc aucun problème de
`file://` — l'application se distribue en deux fichiers : `index.html` (le jeu et le mode examen) et
`decode.html` (le déchiffreur du corrigé QR, hébergé aussi sur
[GitHub Pages](https://fehmitn.github.io/Cour-sante-securite/decode.html)).

---

## 🚀 Lancer le jeu

### Option 1 — Double-clic (le plus simple)

1. Ouvrir le dossier du projet.
2. Double-cliquer sur **`index.html`**.
3. Le jeu s'ouvre dans le navigateur par défaut. C'est tout. 🎉

> Fonctionne avec Chrome, Edge, Firefox et Safari récents. Aucun accès Internet requis, la
> progression est stockée localement.

### Option 2 — Serveur local (recommandé pour modifier le code)

Utile si vous éditez les fichiers, testez sur mobile via le réseau local, ou voulez éviter les
restrictions `file://` de certains navigateurs.

```bash
# Python 3 (souvent déjà installé)
python -m http.server 8000

# ou Node.js
npx serve .

# ou PHP
php -S localhost:8000
```

Puis ouvrir <http://localhost:8000>.

#### Astuce VS Code

Installez l'extension **Live Server**, clic droit sur `index.html` → *Open with Live Server* :
rechargement automatique à chaque sauvegarde.

### 🔗 Liens directs

| Écran | URL |
| :-- | :-- |
| Tableau de bord | `index.html#dashboard` |
| Niveau 1 · Quiz | `index.html#quiz` |
| Niveau 2 · EPI | `index.html#ppe` |
| Niveau 3 · Signaux | `index.html#signals` |
| Mode examen | `index.html#exam` |
| Mémo SST | `index.html#memo` |

---

## 📚 Contenu pédagogique et sources

- **Support de formation** : *Règles de Santé et de Sécurité au Travail* (module M02) — `sst.pdf`.
- **Référentiel graphique** : pictogrammes de sécurité conformes à la norme **ISO 7010**
  (formes et couleurs : obligation, interdiction, danger, secours, lutte incendie), embarqués en
  SVG inline dans `index.html`.
- **Pictogrammes complémentaires** : SVG issus de **Wikimedia Commons** (M004, M009, P003, P010,
  W001, W016, E007, E011, F003, F005), nettoyés puis intégrés directement dans `index.html` — le
  dépôt ne distribue aucun fichier SVG séparé.
- **Pictogrammes de manutention** (pages 44–48 du support) : marques sur les colis (fragile, haut,
  limite de température, empilage, crochets, pinces, diable, chariot à fourches) redessinées en
  SVG inline dans le style normalisé (glyphe noir sur fond clair), et mobilisées dans le quiz
  (banque de 25 questions).
- **Mémo en 3 sous-pages** : `index.html#memo` — pages 1–6 du support (fondamentaux), pages 8–16
  (notions de sécurité, feu-électricité-environnement) et onglet « Équipements & pictogrammes »
  (EPI au style « obligation » ISO 7010, 5 familles de signaux, pictogrammes de manutention).
- **Entête institutionnelle** : « Centre Sectoriel de Formation aux Métiers industriels khnis »
  avec le logo du centre (`logo.svg` vectorisé puis embarqué comme `<symbol id="csfmi-logo">`)
  affichée en haut de l'application, et reprise en tête du **sujet d'examen imprimable**.
- **Parti pris** : contenus reformulés et situations EPI simplifiées à des fins pédagogiques.
  Ce jeu **ne remplace pas** une formation réglementaire, un plan de prévention ou l'avis d'un
  préventeur : il sert à sensibiliser et à réviser.

---

## ♿ Accessibilité et qualité

- Structure HTML sémantique, titres hiérarchisés, `lang="fr"`, lien de navigation par onglets.
- Retours d'action annoncés via `role="status"` / `aria-live="polite"`.
- Boîte de dialogue de réinitialisation en `role="dialog"` + `aria-modal`, fermeture par `Échap`.
- `aria-label` sur les pictogrammes et le travailleur SVG ; focus visibles sur boutons et liens.
- Respect de `prefers-reduced-motion` (animations désactivées si l'utilisateur le demande).
- Responsive sans débordement horizontal, cibles tactiles confortables.
- Mode examen : corrigé masqué par défaut, consignes explicites et impression A4 sur une page
  distincte pour la correction ; les QR du corrigé s'accompagnent d'une légende « Corrigé · page n ».
- Déchiffreur `decode.html` : formulaire étiqueté, message d'erreur explicite sans jamais fuiter le
  corrigé, résultat annoncé via `aria-live`.
- Code sans dépendance : surface d'attaque minimale, aucune donnée envoyée à un serveur.

---

## 🤝 Contribution

Les idées d'amélioration sont bienvenues : nouvelles questions, scénarios EPI supplémentaires,
autres pictogrammes, mode multi-joueurs en salle, export PDF du résultat…

1. Ouvrez une *issue* pour discuter du besoin.
2. Forkez le dépôt, créez une branche (`feature/mon-idee`).
3. Modifiez `index.html` en conservant le style existant (vanilla, sans dépendance).
4. Vérifiez le rendu en `file://` **et** via serveur local, sur mobile et desktop.
5. Proposez une *pull request* avec une capture ou une description du changement.

Dépôt : <https://github.com/fehmitn/Cour-sante-securite>

---

## 📄 Licence et crédits

Le code de l'application est publié sous **licence MIT** — voir le fichier [LICENSE](LICENSE).

```text
MIT License · Copyright (c) 2026 fehmitn
```

**Auteur** : Fehmi Ben Njima — [fehmitn@gmail.com](mailto:fehmitn@gmail.com).

En résumé : utilisation, modification, distribution et usage commercial autorisés, à condition de
conserver la mention de copyright et le texte de la licence. Le logiciel est fourni « en l'état »,
sans garantie.

**Ce que couvre la MIT** : `index.html` (HTML, CSS, JavaScript), `decode.html`, la structure du
document et le code de ce dépôt — à l'exception de la bibliothèque `qrcode-generator` embarquée,
soumise à sa propre licence **MIT** (Copyright (c) 2009 Kazuhiko Arase, mention conservée en tête
du script inline).

**Ce qu'elle ne couvre pas** :

- **Pictogrammes ISO 7010** — symboles intégrés en SVG inline dans `index.html`, dont certains issus
  de **Wikimedia Commons** : symboles normalisés, inclus à des fins pédagogiques et illustratives.
  La norme ISO 7010 reste la propriété de l'ISO ; ils ne constituent pas des marqueurs de sécurité
  officiels.
- **Support de formation** `sst.pdf` (module M02) : document source, repris à titre documentaire.

Le contenu pédagogique (questions, scénarios, fiches mémo) est librement réutilisable dans un cadre
de formation, avec mention du projet. Pour un usage commercial ou une redistribution des
pictogrammes, vérifiez les conditions applicables auprès de l'ISO et de l'auteur du support.

**Attribution suggérée** :

```text
Vigilance SST — https://github.com/fehmitn/Cour-sante-securite — MIT License
Auteur : Fehmi Ben Njima — fehmitn@gmail.com
```

<p align="center">
  <sub>🛡️ <strong>Vigilance SST</strong> — parce que la vigilance s'entraîne aussi. · Fait avec HTML, CSS, JS et beaucoup de pictogrammes. · <a href="LICENSE">Licence MIT</a></sub>
</p>
