# 🛡️ Vigilance SST

### Serious game **Santé & Sécurité au Travail** — 3 niveaux, 290 points de vigilance, 100 % hors-ligne

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
</p>

> **Vigilance SST** est une application web de gamification qui transforme les règles de santé et de
> sécurité au travail en un parcours ludique : un quiz sur les fondamentaux, des scénarios
> d'équipement EPI et un jeu de reconnaissance des signaux ISO 7010.
>
> Un seul fichier, aucun serveur, aucune installation : **double-cliquez, jouez, progressez.**

---

## 📑 Sommaire

- [🎯 Le projet](#-le-projet)
- [✨ Fonctionnalités](#-fonctionnalités)
- [🎮 Le parcours en 3 niveaux](#-le-parcours-en-3-niveaux)
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
| Ancrer les définitions (accident, maladie professionnelle, feu, EPI) | 🔍 Quiz de 10 questions avec explication systématique |
| Faire le lien entre risque et protection | 🧰 3 situations de travail à équiper correctement |
| Reconnaître les familles de signaux d'un coup d'œil | ⚡ Flash de 12 s sur 10 pictogrammes ISO 7010 |
| Donner envie de rejouer | 🏆 290 PV, 5 rangs, 5 badges, meilleurs scores conservés |
| Rester utilisable en salle, sans réseau | 📴 Fichier local, aucune dépendance externe |

Public visé : nouveaux arrivants, sensibilisation annuelle, ateliers de prévention, étudiants en
hygiène-sécurité, formateurs cherchant un support d'ouverture ou de révision.

---

## ✨ Fonctionnalités

- 🧭 **Tableau de bord unifié** — score global, anneau de progression, rang courant et état des 3 niveaux.
- 🎯 **Parcours progressif** — les niveaux s'enchaînent, mais restent accessibles librement (navigation par onglets).
- 💾 **Progression persistante** — meilleurs scores sauvegardés dans `localStorage` (clé `vigilance_sst_v1`), appareil par appareil.
- 🔁 **Rejouabilité** — chaque tentative peut améliorer le record ; le score total ne régresse jamais.
- 🧾 **Feedback pédagogique** — chaque réponse est expliquée (bonne ou mauvaise), sans jamais laisser l'apprenant deviner.
- ⏱️ **Chrono temps réel** — niveau 3, 12 secondes par signal, barre qui passe en alerte à 4 s.
- 🏅 **Rangs et badges** — 5 paliers de « Observateur » à « Légende SST » et 5 badges de réussite.
- 🧰 **Visuel EPI interactif** — un travailleur SVG réagit aux équipements sélectionnés.
- 📱 **Responsive** — grilles fluides du mobile au grand écran, barre supérieure collante.
- ♿ **Accessible** — HTML sémantique, `aria-live` sur les retours, `aria-modal`, focus visibles, `prefers-reduced-motion`.
- 🖨️ **Mémo imprimable** — fiche de révision « L'essentiel SST » consultable à tout moment.
- 🔗 **Routes par ancre** — `#dashboard`, `#quiz`, `#ppe`, `#signals`, `#memo` : chaque écran est partageable.

---

## 🎮 Le parcours en 3 niveaux

| # | Niveau | Mécanique | Contenu | Barème |
| :-: | :-- | :-- | :-- | :-- |
| **01** | 🔍 **Les fondamentaux** | Quiz à choix unique, correction expliquée | 10 questions : définitions, droits et obligations, feu, prévention | 10 PV / bonne réponse → **100 PV** |
| **02** | 🧰 **Bien s'équiper** | Sélection multiple d'EPI sur 3 situations | Chantier extérieur · Travail en hauteur · Laboratoire | 10 PV / EPI correct, −5 PV / EPI inutile → **90 PV** |
| **03** | ⚡ **L'œil du safety** | Reconnaissance de famille sous contrainte de temps | 10 pictogrammes, 5 familles ISO 7010 | 10 PV / signal en moins de 12 s → **100 PV** |
| | | | **Total** | **290 PV** |

### 01 · 🔍 Quiz SST — « Les fondamentaux »

- 10 questions, une seule bonne réponse, validation puis correction immédiate.
- Chaque question est accompagnée d'une **explication courte** issue du support de formation.
- Panneau latéral : liste des questions avec ✓ pour celles déjà maîtrisées (meilleur score).
- Écran de fin : bonnes réponses, meilleur score, message adapté (≥ 80 %, ≥ 50 %, sinon révision du mémo).

### 02 · 🧰 Équipez le travailleur

Trois scénarios, trois risques, trois EPI indispensables à chaque fois :

| Scénario | Risques | EPI attendus |
| :-- | :-- | :-- |
| 🏗️ **Chantier extérieur** — déchargement de palettes | Chute d'objets, coupures, écrasement des pieds | Casque, gants, chaussures de sécurité |
| 🪜 **Travail en hauteur** — contrôle sur échafaudage | Chute de hauteur, chute d'outils, perte d'équilibre | Casque, chaussures de sécurité, harnais antichute |
| 🧪 **Laboratoire** — manipulation de produit chimique | Projections, contact cutané, vapeurs irritantes | Gants chimiques, lunettes, masque respiratoire |

Le calcul est volontairement nuancé : **+10 PV** par EPI attendu, **−5 PV** par EPI superflu,
score borné entre 0 et 30 par scénario. Le meilleur résultat est conservé.

### 03 · ⚡ Reconnaissance des signaux

Dix pictogrammes, cinq familles, douze secondes. La réponse est un clic sur la famille perçue :

| Famille | Forme et couleur | Exemple |
| :-- | :-- | :-- |
| 🔵 **Obligation** | Rond bleu, inscription blanche | Porter un casque · Protection auditive |
| 🔴 **Interdiction** | Rond blanc, contour rouge, cercle barré | Interdiction de fumer · Téléphone interdit |
| 🟡 **Danger** | Triangle jaune, inscription noire | Danger électrique · Risque d'incendie |
| 🟢 **Secours** | Carré vert, inscription blanche | Premiers secours · Civière |
| 🧯 **Incendie** | Carré rouge, inscription blanche | Extincteur · Boyau d'incendie |

À l'expiration du chrono, la réponse est comptée fausse — mais le pictogramme et sa famille sont
toujours expliqués, pour transformer l'erreur en apprentissage.

---

## 🏅 Score, rangs et badges

**Points de Vigilance (PV)** : 290 au maximum, affichés en permanence dans la barre supérieure et le pied de page.

| Rang | Seuil | Message |
| :-- | :-: | :-- |
| 👀 Observateur | 0 PV | Le point de départ de toute vigilance |
| 🟢 Vigilant | 60 PV | Les réflexes commencent à s'installer |
| 🛡️ Gardien SST | 140 PV | Vous savez reconnaître et prévenir |
| 🎓 Expert SST | 220 PV | Les fondamentaux sont solides |
| 🏆 Légende SST | 290 PV | Parcours complet, sans faute |

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
| **SVG** | Pictogrammes **ISO 7010** en `viewBox` 265×265 / 200×200, sprite `<symbol>` inline, travailleur et jauges animés |
| **localStorage** | Persistance `vigilance_sst_v1` : meilleurs scores, niveaux terminés, réinitialisation |

> 🧊 **Zéro dépendance, zéro requête réseau.** Pas de CDN, pas de police distante, pas de
> `npm install` : l'application est un unique fichier `index.html` autonome (~131 Ko).

---

## 📁 Arborescence

```text
Cour-sante-securite/
├── index.html                    # Application complète : HTML + CSS + JS + pictogrammes inline
├── README.md                     # Ce document
├── s01.svg                       # Civière de premiers secours
├── Boyau d'incendie.svg          # Signal incendie
├── Danger électrique.svg         # Signal danger
├── Extincteur.svg                # Signal incendie
├── Interdiction de fumer.svg     # Signal interdiction
├── Premiers secours.svg          # Signal secours
├── Protection auditive.svg       # Signal obligation
├── Risque d'incendie.svg         # Signal danger
├── Téléphone interdit.svg        # Signal interdiction
├── sante securite.zip            # Archive des pictogrammes sources
└── sst.pdf                       # Support de formation M02 (source pédagogique)
```

Les SVG à la racine sont les **sources vectorielles** des pictogrammes ; dans l'application, ils sont
intégrés en inline (aucun chargement de fichier externe, donc aucun problème de `file://`).

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
| Mémo SST | `index.html#memo` |

---

## 📚 Contenu pédagogique et sources

- **Support de formation** : *Règles de Santé et de Sécurité au Travail* (module M02) — `sst.pdf`.
- **Référentiel graphique** : pictogrammes de sécurité conformes à la norme **ISO 7010**
  (formes et couleurs : obligation, interdiction, danger, secours, lutte incendie).
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

- **Application** : projet pédagogique, code et contenus rédigés pour la sensibilisation SST.
  Contactez l'auteur pour toute réutilisation en dehors d'un cadre de formation.
- **Pictogrammes ISO 7010** : symboles normalisés, repris des fichiers SVG fournis dans ce dépôt
  (`sante securite.zip`). La norme ISO 7010 reste la propriété de l'ISO ; ces visuels sont utilisés
  à des fins illustratives et pédagogiques.
- **Source documentaire** : `sst.pdf`, support de formation interne (module M02).

<p align="center">
  <sub>🛡️ <strong>Vigilance SST</strong> — parce que la vigilance s'entraîne aussi. · Fait avec HTML, CSS, JS et beaucoup de pictogrammes.</sub>
</p>
