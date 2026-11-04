# Prompts de plans — [MARQUE] — [TITRE]

> **Mode d'emploi.** Copier ce modèle vers `campagnes/AAAA-MM-marque-objet/04-prompts.md`. Ce fichier ne concerne que les plans **générés** ou **hybrides**. Les prompts sont écrits **en anglais** (meilleurs résultats avec la plupart des modèles). Ne jamais demander à un modèle d'écrire un texte ou un logo : on les ajoute au montage.
>
> Statut : ☐ Brouillon ☐ En test ☐ **Plans validés** — Date : [date]

---

## 1. Méthode

1. **Image de référence d'abord.** On génère une image fixe du plan, on la valide, puis on la met en mouvement. C'est plus fiable que de partir directement du texte.
2. **Un plan = un mouvement de caméra** de 2 à 5 secondes.
3. **Bible visuelle copiée telle quelle** au début de chaque prompt.
4. **On note chaque essai** (outil, paramètres, résultat) pour ne pas gaspiller le quota gratuit quotidien.

## 2. Bible visuelle de la campagne

*Description fixe, réutilisée au début de chaque prompt.*

- **Produit** (copié de la fiche marque, en anglais) :
- **Personnage(s)** (âge, traits, vêtements, coiffure — ou « aucun visage visible ») :
- **Décor récurrent :**
- **Lumière récurrente :**
- **Palette :**
- **Optique et rendu** (ex. : 85 mm look, shallow depth of field, subtle film grain) :
- **Style général** (ex. : photorealistic, commercial cinematography) :

**Bloc à coller au début de chaque prompt :**

```text
[Product description]. [Character description]. [Setting]. [Lighting]. [Palette]. [Lens and look]. [Overall style].
```

## 3. Formule d'un prompt

```text
[Bloc bible visuelle] + [Sujet et action] + [Cadrage et angle] + [Mouvement de caméra, lent et unique] + [Lumière et ambiance du plan] + [Effets] + [Contraintes de réalisme]
```

- **Contraintes de réalisme utiles :** steady camera, natural motion, no cuts, photorealistic, 24 fps cinematic look.
- **Prompt négatif de base :** text, logo, watermark, subtitles, distorted object, extra objects, deformed hands, flicker, fast motion, blurry, low quality.

## 4. Journal des outils et paramètres

- **Outil d'images :** [nom, lien] — licence : [type] — vérifiée le : [date]
- **Outil de vidéo :** [nom, lien] — licence : [type] — vérifiée le : [date]
- **Quota restant / limites du jour :**
- **Format et résolution demandés :**

---

## 5. Plans

*Dupliquer le bloc pour chaque plan.*

### PLAN 01 — [nom court]

- **Lien storyboard :** plan 01 — durée [x] s — source GÉNÉRÉ / HYBRIDE
- **Objectif du plan :**
- **Prompt de l'image de référence :**
  ```text
  [prompt en anglais]
  ```
- **Image validée :** [chemin ou lien] — ☐ validée
- **Prompt de mise en mouvement :**
  ```text
  [prompt en anglais : mouvement de caméra + mouvement naturel du sujet]
  ```
- **Prompt négatif :**
  ```text
  [prompt négatif]
  ```
- **Paramètres :** durée [x] s — format [16:9 / 9:16] — résolution [ ] — graine / seed [ ]
- **Essais :**
  - Essai 1 — [date] — résultat : [bon / défaut] — remarque :
  - Essai 2 —
- **Retenu :** [fichier ou lien]
- **Retouches au montage prévues :** [logo, texte, étalonnage, accéléré, ralenti]
- **Statut :** ☐ à faire ☐ en cours ☐ à refaire ☐ validé

### PLAN 02 — [nom court]

- **Lien storyboard :**
- **Objectif du plan :**
- **Prompt de l'image de référence :**
  ```text
  ```
- **Image validée :**
- **Prompt de mise en mouvement :**
  ```text
  ```
- **Prompt négatif :**
  ```text
  ```
- **Paramètres :**
- **Essais :**
- **Retenu :**
- **Retouches au montage prévues :**
- **Statut :** ☐ à faire ☐ en cours ☐ à refaire ☐ validé

---

## 6. Exemple rempli (marque fictive)

*Exemple pédagogique avec une marque inventée, « Source Aurore ». À supprimer dans un vrai fichier de campagne.*

**Bible visuelle**

```text
A glass bottle of mineral water with a plain blank blue label, condensation on the glass, silver screw cap. Wet black slate surface. Early morning light from a window on the left, soft rim light on the glass edges. Cool blue and silver palette. 85 mm lens look, shallow depth of field, subtle film grain. Photorealistic commercial cinematography.
```

**Plan 01 — Révélation du produit (4 s)**

- **Prompt de l'image de référence :**
  ```text
  A glass bottle of mineral water with a plain blank blue label, condensation on the glass, silver screw cap, standing on a wet black slate surface. Early morning light from a window on the left, soft rim light on the glass edges. Cool blue and silver palette. Close-up, eye-level angle, 85 mm lens look, shallow depth of field, subtle film grain. Photorealistic commercial cinematography.
  ```
- **Prompt de mise en mouvement :**
  ```text
  Slow push-in toward the bottle, water droplets sliding down the glass, soft shimmer of light on the wet slate, steady camera, natural motion, no cuts, 24 fps cinematic look.
  ```
- **Prompt négatif :**
  ```text
  text, logo, watermark, subtitles, distorted bottle, extra objects, flicker, fast motion, blurry, low quality
  ```
- **Retouches au montage :** logo et nom ajoutés sur l'étiquette vierge (ou plan remplacé par un vrai packshot), étalonnage froid, grain léger.
