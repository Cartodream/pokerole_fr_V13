# Mise à jour Pokérole pour Foundry VTT V13

Ce document décrit les modifications apportées pour rendre le système Pokérole compatible avec Foundry VTT V13.

## Modifications effectuées

### 1. Compatibilité système (system.json)
- Mise à jour de la compatibilité minimum de V10 à V12
- Mise à jour de la version vérifiée de "12.331" à "13"
- Mise à jour de la version maximum de 12 à 13
- Mise à jour de la version du système à "0.4.3-v13"

### 2. Corrections API Foundry V13

#### module/documents/item.mjs
- Correction de `ChatMessage.getSpeaker` vers `ChatMessage.implementation.getSpeaker`

#### module/documents/actor.mjs
- Correction de `getProperty` vers `foundry.utils.getProperty`
- Correction de `mergeObject` vers `foundry.utils.mergeObject`

#### module/helpers/roll.mjs
- Correction de tous les appels `ChatMessage.create` vers `ChatMessage.implementation.create`

#### module/helpers/damage.mjs
- Correction de `Actor.implementation.get` vers `game.actors.get`

### 3. Fichier CSS minimal
- Création d'un fichier CSS minimal (`css/pokerole.css`) pour assurer le fonctionnement de base
- Styles pour les boutons d'action, compteurs de combat, et affichage des dés

## Installation

1. Copiez ce dossier dans votre répertoire de systèmes Foundry VTT
2. Le système devrait maintenant être compatible avec Foundry V13

## Notes importantes

- Cette mise à jour maintient la compatibilité avec V12 (minimum V12)
- Le fichier CSS est minimal - pour une expérience complète, compilez les fichiers SCSS avec `npm run build`
- Toutes les fonctionnalités principales du système devraient fonctionner normalement

## Compilation CSS (optionnel)

Si vous souhaitez compiler les fichiers SCSS complets :

```bash
npm install
npm run build
```

## Problèmes connus

Aucun problème majeur identifié. Le système devrait fonctionner normalement avec Foundry V13.