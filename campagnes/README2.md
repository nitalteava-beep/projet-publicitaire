# Campagnes

Ce dossier contient **un sous-dossier par campagne publicitaire**.

## Nommer une campagne

`AAAA-MM-marque-objet`, en minuscules, avec des tirets et sans accents.

Exemples : `2026-11-source-aurore-lancement`, `2027-02-atelier-nord-promo-hiver`.

## Contenu d'un dossier de campagne

```text
campagnes/2026-11-source-aurore-lancement/
├── 01-brief.md          ← modèle : modeles/02-brief.md
├── 02-script.md         ← modèle : modeles/03-script.md
├── 03-storyboard.md     ← modèle : modeles/04-storyboard.md
├── 04-prompts.md        ← modèle : modeles/05-prompts-plans.md
└── 05-livraison.md      ← modèle : modeles/06-checklist-qualite.md
```

## Démarrer une campagne

1. Vérifier que la fiche de la marque existe dans `marques/`.
2. Créer le dossier de la campagne en ajoutant un premier fichier avec son chemin complet, par exemple `campagnes/2026-11-source-aurore-lancement/01-brief.md`.
3. Remplir et faire valider le brief, puis suivre l'ordre des fichiers.

## Où mettre les vidéos ?

Pas dans le dépôt : elles sont trop lourdes (envoi par navigateur limité à 25 Mo par fichier, blocage au-delà de 100 Mo à ce jour). Les stocker dans un cloud personnel ou dans les *Releases* GitHub, puis noter les liens dans `05-livraison.md`.

## Confidentialité

Le dépôt est public. Pour un client sensible, utiliser un dépôt privé.
