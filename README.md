# 🎬 Atelier de création publicitaire cinématique

> Cahier des charges et boîte à outils de notre atelier : concevoir des publicités **réalistes, professionnelles et cinématiques**, avec des moyens **gratuits et open source**, depuis un **smartphone Android**.

**Version 1.0 — 4 novembre 2026**

---

## Sommaire

1. [Mission et objectifs](#1-mission-et-objectifs)
2. [Principes et contraintes de l'atelier](#2-principes-et-contraintes-de-latelier)
3. [Répartition des rôles](#3-répartition-des-rôles)
4. [Processus de création en 7 étapes](#4-processus-de-création-en-7-étapes)
5. [Structure du dépôt](#5-structure-du-dépôt)
6. [Conventions de travail](#6-conventions-de-travail)
7. [Boîte à outils gratuite et open source](#7-boîte-à-outils-gratuite-et-open-source)
8. [Standard de réalisme cinématographique](#8-standard-de-réalisme-cinématographique)
9. [Droits, éthique et confidentialité](#9-droits-éthique-et-confidentialité)
10. [Travailler depuis Android](#10-travailler-depuis-android)
11. [Démarrer une nouvelle campagne](#11-démarrer-une-nouvelle-campagne)
12. [Limites connues et évolutions](#12-limites-connues-et-évolutions)

---

## 1. Mission et objectifs

**Mission.** Transformer un besoin commercial (lancer un produit, promouvoir un service, soutenir une marque) en une publicité courte dont l'image, le rythme et le son atteignent une **qualité commerciale** : on doit y croire, la regarder jusqu'au bout, et retenir la marque.

**Objectifs de l'atelier**

- Produire des publicités de 6 à 60 secondes avec une vraie grammaire de cinéma : mouvements de caméra maîtrisés, lumière intentionnelle, étalonnage cohérent, sound design soigné.
- Standardiser le travail : chaque campagne suit le même parcours (brief → script → storyboard → plans → montage → livraison).
- Rester reproductible : tout ce qui est décidé est écrit dans ce dépôt, pour ne jamais repartir de zéro.
- Garder un coût proche de zéro, sans dépendre d'un outil propriétaire unique.

**Ce que l'atelier livre pour chaque campagne**

| Livrable | Description |
|---|---|
| Brief validé | Cadre de la campagne, signé par le client ou l'équipe |
| Script | Le déroulé image, son, voix et texte |
| Storyboard et liste de plans | Chaque plan décrit techniquement |
| Prompts de plans | Instructions prêtes à l'emploi pour générer les images et vidéos |
| Film final | Vidéo(s) aux formats demandés |
| Registre des droits | Preuve de licence de chaque élément utilisé |

---

## 2. Principes et contraintes de l'atelier

| Contrainte | Conséquence concrète |
|---|---|
| **Smartphone Android en priorité** | Tout doit pouvoir se faire (ou se préparer) depuis un téléphone : fichiers texte courts, formats simples, tableaux évités au profit de blocs lisibles sur petit écran. |
| **Claude en version gratuite** | Les échanges ont des limites d'usage : on travaille étape par étape, avec un seul livrable par conversation et en collant uniquement les modèles utiles. |
| **GitHub comme mémoire de l'atelier** | Texte et modèles dans le dépôt. Les vidéos lourdes restent hors du dépôt (voir §6). |
| **Gratuit et open source en priorité** | On choisit d'abord un outil libre. Un outil gratuit non libre est accepté s'il n'existe pas d'équivalent libre utilisable sur Android, et il est signalé comme tel. |
| **Remotion exclu** | Remotion n'est pas utilisé dans cet atelier. Les titres, sous-titres et logos animés se font dans l'éditeur vidéo ; l'assemblage technique peut passer par FFmpeg si besoin. |
| **Usage commercial** | Chaque outil et chaque ressource doit avoir une licence qui autorise l'usage publicitaire. Sans preuve, on ne l'utilise pas. |
| **Réalisme avant tout** | On préfère un plan simple et crédible à un plan spectaculaire raté. Voir §8. |

---

## 3. Répartition des rôles

**Claude (version gratuite)** rédige et structure : fiches marque, briefs, concepts, scripts, storyboards, listes de plans, prompts de génération, checklists, textes à l'écran, voix off. Claude **ne génère pas de vidéo** dans cet atelier : il prépare tout ce qui permet d'en produire une de bonne qualité.

**L'humain (vous)** décide, filme, valide et assemble : choix du concept, tournage des plans réels au smartphone, lancement des générations, montage, validation finale, respect des droits.

**Les outils** génèrent les images et vidéos, enregistrent les voix, montent et exportent (voir §7).

---

## 4. Processus de création en 7 étapes

Chaque étape produit un fichier dans le dossier de la campagne (voir §5). On ne passe à l'étape suivante que lorsque la précédente est validée.

### Étape 0. Cadrage de la marque
Fiche marque : identité, ton, couleurs, interdits, description fidèle du produit.
📄 `marques/nom-marque.md` — modèle : `modeles/01-fiche-marque.md`

### Étape 1. Brief
Objectif mesurable, cible, message unique, formats, contraintes, références visuelles.
📄 `campagnes/<campagne>/01-brief.md` — modèle : `modeles/02-brief.md`

### Étape 2. Concept et script
Une idée forte, résumable en une phrase, puis le déroulé complet (accroche, développement, révélation du produit, appel à l'action).
📄 `campagnes/<campagne>/02-script.md` — modèle : `modeles/03-script.md`

### Étape 3. Storyboard et liste de plans
Chaque plan reçoit : durée, valeur de plan, angle, optique, mouvement, lumière, source (filmé, généré ou hybride).
📄 `campagnes/<campagne>/03-storyboard.md` — modèle : `modeles/04-storyboard.md`

### Étape 4. Prompts de plans
Pour chaque plan généré : prompt de l'image de référence, prompt de mise en mouvement, prompt négatif, paramètres.
📄 `campagnes/<campagne>/04-prompts.md` — modèle : `modeles/05-prompts-plans.md`

### Étape 5. Production et montage
Tournage des plans réels, génération des plans IA, voix off, musique, montage, étalonnage, mixage. Les fichiers lourds restent hors du dépôt ; on note leur emplacement.

### Étape 6. Contrôle qualité et livraison
Checklist technique, artistique, juridique, puis export aux formats demandés.
📄 `campagnes/<campagne>/05-livraison.md` — modèle : `modeles/06-checklist-qualite.md`

> **Mode hybride recommandé.** Pour un rendu vraiment réaliste, la meilleure méthode gratuite consiste à **filmer le vrai produit au smartphone** (lumière de fenêtre, fond propre, mouvements lents) et à utiliser la génération pour les plans d'ambiance, les décors, les effets et les transitions. Un produit réel garde ses vrais logos, ses vraies textures et ses vraies proportions, ce que les modèles génératifs reproduisent mal.

---

## 5. Structure du dépôt

```text
projet-publicitaire/
├── README.md                      ← ce cahier des charges
├── modeles/                       ← modèles à copier pour chaque campagne
│   ├── 01-fiche-marque.md
│   ├── 02-brief.md
│   ├── 03-script.md
│   ├── 04-storyboard.md
│   ├── 05-prompts-plans.md
│   └── 06-checklist-qualite.md
├── marques/                       ← une fiche par marque
│   └── README.md
├── campagnes/                     ← un dossier par campagne
│   └── README.md
└── ressources/
    └── glossaire-cinema.md        ← vocabulaire caméra, lumière, montage, son
```

Structure type d'une campagne :

```text
campagnes/2026-11-nom-marque-lancement/
├── 01-brief.md
├── 02-script.md
├── 03-storyboard.md
├── 04-prompts.md
└── 05-livraison.md                ← checklist, liens des vidéos, registre des droits
```

---

## 6. Conventions de travail

**Noms de fichiers et de dossiers.** Minuscules, tirets, sans accents ni espaces (`source-aurore`, pas `Source Aurore`).

**Nom d'une campagne.** `AAAA-MM-marque-objet`, par exemple `2026-11-source-aurore-lancement`.

**Versions.** On ne renomme pas les fichiers pour marquer une version. On modifie le fichier ; l'historique GitHub conserve les anciennes versions. Pour garder une alternative, on crée `02-script-v2.md`.

**Messages de commit.** Courts et clairs : `Ajoute le brief source-aurore`, `Corrige le plan 4 du storyboard`.

**Langue.** Documents en français. Les prompts de génération sont écrits en anglais, car la plupart des modèles y répondent mieux ; la version française reste dans le script.

**Formats vidéo de référence.**

| Usage | Format | Résolution |
|---|---|---|
| Écran large (TV, YouTube, site) | 16:9 | 1920 × 1080 |
| Réseaux verticaux (Reels, TikTok, Shorts) | 9:16 | 1080 × 1920 |
| Fil d'actualité | 4:5 ou 1:1 | 1080 × 1350 ou 1080 × 1080 |

Cadence : 24 ou 25 images par seconde pour un rendu cinéma ; 30 si le client l'impose. Durées usuelles : 6 s, 15 s, 30 s, 60 s.

**Fichiers lourds.** Les vidéos finales ne vont pas dans le dépôt : à ce jour, l'envoi par navigateur est limité à 25 Mo par fichier, et GitHub bloque les fichiers de plus de 100 Mo. On stocke les vidéos dans un cloud personnel ou dans les *Releases* GitHub, et on note le lien dans `05-livraison.md`. Ces limites peuvent évoluer : les revérifier au besoin.

---

## 7. Boîte à outils gratuite et open source

*Statut vérifié le 4 novembre 2026. Les licences, quotas et offres gratuites changent souvent : **revérifier avant chaque campagne commerciale** et consigner la preuve dans `05-livraison.md`.*

### 7.1 Génération d'images (plans de référence)

| Outil | Licence | Usage commercial |
|---|---|---|
| **FLUX.1 [schnell]** (Black Forest Labs) | Apache 2.0 | Autorisé (usages interdits listés : contenus illégaux, harcèlement, désinformation à grande échelle, nudité non consensuelle) |

### 7.2 Génération de vidéo

| Modèle | Licence | Usage commercial | Remarque |
|---|---|---|---|
| **Wan 2.2** (Alibaba) | Apache 2.0 | Autorisé | Demande un GPU : à utiliser via un service en ligne, pas sur le téléphone |
| **LTX-2.3** (Lightricks) | Licence communautaire LTX-2 | Gratuit pour les organisations sous 10 M$ de chiffre d'affaires ; licence commerciale au-delà | À relire avant usage client |
| **HunyuanVideo 1.5** (Tencent) | Licence communautaire Tencent | Autorisé sous conditions propres | Lire attentivement la licence (seuils d'utilisateurs, éventuelles restrictions territoriales) |

**Accès sans GPU personnel.** Les *Spaces ZeroGPU* de Hugging Face permettent d'essayer ces modèles depuis un navigateur mobile. Le quota gratuit est **petit** : environ 5 minutes de GPU par jour avec un compte gratuit, 2 minutes sans compte, remis à zéro 24 h après la première utilisation. Conséquence : on ne génère qu'un nombre limité de plans par jour, on prépare donc les prompts à l'avance (étape 4) pour ne pas gaspiller de quota.

### 7.3 Voix off

| Outil | Licence | Remarque |
|---|---|---|
| **Kokoro** (modèle de 82 M de paramètres) | Apache 2.0 | Gère le français. Utile pour les maquettes et les tests. Pour une publicité finale de qualité commerciale, préférer une **vraie voix enregistrée au smartphone** (pièce calme, micro proche, écran anti-pop improvisé). |

### 7.4 Montage et étalonnage sur Android

Aucun éditeur vidéo open source mûr n'a pu être confirmé sur Android. Les éditeurs libres établis (Kdenlive, Shotcut, OpenShot) fonctionnent sur ordinateur. Options retenues :

| Outil | Open source | Remarque |
|---|---|---|
| **OpenCut** | Oui (MIT) | Éditeur web, traitement local dans le navigateur, sans compte. Version 0.3.0 : à **tester sur le téléphone** avant de lui confier une campagne ; l'absence de filigrane est à vérifier. |
| **VN Video Editor** | Non | Gratuit sur Android, sans filigrane massif ; une carte de fin « Made with VN » peut s'ajouter et se supprime avant l'export. |
| **CapCut** | Non | Gratuit mais la version gratuite est limitée ; beaucoup de fonctions utiles sont réservées à l'abonnement. |
| **Kdenlive, Shotcut, OpenShot** | Oui | Ordinateur uniquement : à utiliser si un PC est disponible pour un montage plus poussé. |
| **FFmpeg** (via Termux, optionnel) | Oui | Pour assembler, convertir ou compresser en ligne de commande. Niveau avancé. |

### 7.5 Musique et effets sonores

Utiliser uniquement des sons dont la licence autorise l'usage commercial publicitaire. Pour chaque morceau : nom, auteur, lien, type de licence, capture d'écran de la page de licence, dans le registre des droits.

### 7.6 Écriture et préparation

**Claude (version gratuite)** pour tous les documents du dépôt. **GitHub** pour la mémoire et l'historique.

---

## 8. Standard de réalisme cinématographique

Ces règles s'appliquent à chaque plan, qu'il soit filmé ou généré.

**Caméra et mouvement**

- **Un seul mouvement de caméra par plan**, lent et motivé. Les mouvements complexes ou rapides sont ceux que les modèles génératifs réussissent le moins bien.
- Choisir le mouvement selon l'intention :

| Intention | Mouvement |
|---|---|
| Révéler le produit | Travelling avant lent (*push-in*) |
| Donner de la puissance | Contre-plongée, orbite lente autour du sujet |
| Situer le contexte | Plan large, grue ascendante |
| Créer de l'intimité | Plan serré, faible profondeur de champ |
| Donner du rythme | Travelling latéral, panoramique filé (*whip pan*) comme transition |

- Plans courts : **2 à 5 secondes**. Un plan généré plus long perd en cohérence.
- Rendu cinéma : 24 ou 25 images par seconde, léger flou de mouvement naturel.

**Lumière**

- Lumière **motivée** : on doit deviner d'où elle vient (fenêtre, lampe, soleil bas).
- Schéma de base : lumière principale, lumière de remplissage douce, contre-jour ou lumière de bord pour détacher le sujet.
- Heures privilégiées en extérieur : heure dorée et heure bleue.

**Image et couleur**

- Palette limitée : 2 à 3 couleurs dominantes plus la couleur d'accent de la marque.
- Étalonnage **cohérent sur tous les plans** de la campagne, avec un grain léger et une vignette discrète.
- Profondeur de champ crédible : fond adouci sur les plans serrés, netteté plus large sur les plans larges.

**Cohérence**

- Chaque campagne définit une **bible visuelle** (description fixe du produit, des personnages, du décor, du style) reprise **mot pour mot** au début de chaque prompt.
- On génère d'abord une **image de référence** (*keyframe*) validée, puis on la met en mouvement. C'est plus fiable que de demander une vidéo directement à partir du texte.

**Pièges connus à contourner**

- **Textes et logos** : ne jamais demander à un modèle de les écrire. On les ajoute au montage, nets et exacts.
- **Mains, visages en gros plan, foules** : cadrer de dos, en silhouette, en plan large ou en détail partiel pour limiter les défauts.
- **Produit déformé** : filmer le vrai produit ou le montrer en image fixe réelle avec un mouvement ajouté au montage.
- **Son** : une grande partie de l'impression de qualité vient du son. Ne pas livrer sans ambiance, bruitages et mixage soignés.

Le vocabulaire complet est dans `ressources/glossaire-cinema.md`.

---

## 9. Droits, éthique et confidentialité

- **Confidentialité.** Ce dépôt est **public** : tout le monde peut lire son contenu. Ne pas y publier d'informations confidentielles d'un client (chiffres, lancements non annoncés, contrats). Pour un client sensible, passer le dépôt en privé (réglages du dépôt, rubrique visibilité) ou créer un dépôt privé dédié.
- **Licences.** Chaque outil, modèle, police, musique, son et image tierce doit avoir une licence autorisant l'usage commercial. La preuve est notée dans le registre des droits de la campagne.
- **Personnes réelles.** Ne pas reproduire le visage, la voix ou le style identifiable d'une personne réelle sans son accord écrit. Pas de célébrités ni de sosies.
- **Marques et œuvres tierces.** Ne pas montrer de marques concurrentes ni de personnages ou œuvres protégés, sauf autorisation.
- **Transparence.** Si une plateforme ou la réglementation impose d'indiquer qu'un contenu est généré ou retouché par IA, l'indiquer. Une publicité ne doit jamais induire en erreur sur le produit ni sur ses performances.
- **Mentions légales.** Les mentions obligatoires du secteur (santé, alimentation, finance, alcool, etc.) figurent dans la fiche marque et sont vérifiées à la livraison.
- **Contenus interdits.** Aucun contenu illégal, haineux, trompeur ou portant atteinte à la dignité des personnes.

---

## 10. Travailler depuis Android

**Ajouter un fichier au dépôt (méthode simple)**

1. Ouvrir le dépôt dans le navigateur du téléphone. Si l'écran est trop étroit, activer « Version pour ordinateur » dans le menu du navigateur.
2. Appuyer sur **Add file**, puis **Create new file**.
3. Dans le champ du nom, **taper le chemin complet** : `modeles/02-brief.md`. Les dossiers manquants se créent automatiquement quand on tape `/`.
4. Coller le contenu, puis **Commit changes** (message court, par exemple « Ajoute le modèle de brief »).

**Déplacer ou renommer un fichier.** Ouvrir le fichier, choisir l'édition, puis modifier son nom en y ajoutant le dossier (`brief.md` devient `modeles/02-brief.md`) et valider.

**Utiliser Claude efficacement en version gratuite**

- Un livrable par conversation : « Rédige le script » plutôt que « fais toute la campagne ».
- Coller seulement la fiche marque, le brief et le modèle nécessaires.
- Demander à Claude de répondre **dans le format du modèle**, prêt à copier dans le fichier.
- Si le projet Claude synchronise le dépôt, vérifier que les dossiers utiles (`modeles/`, `marques/`, `campagnes/`) sont bien inclus, et pas seulement `README.md`.

**Filmer correctement au smartphone**

- Orientation et format choisis **avant** de filmer (voir §6).
- Lumière naturelle de fenêtre, source unique, pas de flash.
- Verrouiller l'exposition et la mise au point ; utiliser le mode vidéo à 24 ou 30 images par seconde.
- Mouvements lents, téléphone appuyé ou posé sur un support stable ; un petit trépied ou un support improvisé suffit.

---

## 11. Démarrer une nouvelle campagne

1. Créer ou mettre à jour la fiche marque dans `marques/` (copie de `modeles/01-fiche-marque.md`).
2. Créer le dossier `campagnes/AAAA-MM-marque-objet/`.
3. Copier `modeles/02-brief.md` vers `01-brief.md` dans ce dossier, le remplir (avec Claude si besoin), le faire valider.
4. Enchaîner : script, storyboard, prompts, production, livraison.

**Phrase type à donner à Claude, étape par étape :**

```text
Voici la fiche marque : [coller]
Voici le brief validé : [coller]
Rédige le script de 30 secondes en suivant exactement ce modèle : [coller modeles/03-script.md]
Standard de réalisme : un seul mouvement de caméra par plan, plans de 2 à 5 secondes.
Propose d'abord 3 concepts en une phrase chacun ; je choisis, puis tu écris le script.
```

---

## 12. Limites connues et évolutions

- **Quotas gratuits limités.** La génération vidéo en ligne gratuite impose un petit budget par jour. La production se planifie sur plusieurs jours ou se complète par des plans filmés.
- **Montage sur Android.** Aucun éditeur libre mature confirmé sur téléphone ; le choix de l'éditeur est à réévaluer régulièrement.
- **Voix.** Les voix synthétiques gratuites conviennent aux maquettes ; la qualité commerciale demande une voix humaine.
- **Licences mouvantes.** Chaque modèle peut changer de licence : consigner la version et la date d'usage.

**Évolutions prévues** : exemple de campagne complète, bibliothèque de prompts éprouvés, LUTs d'étalonnage libres, liste de musiques et sons à licence claire, fiches de retour d'expérience après chaque campagne.

---

*Ce document est vivant. Toute décision d'atelier (outil adopté, règle modifiée, leçon apprise) est écrite ici ou dans un fichier du dépôt, avec la date.*
