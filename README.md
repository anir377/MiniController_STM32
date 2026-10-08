# MiniController STM32 — Projet PCB 5A Polytech

Projet issu du modèle **Projet_PCB_FISE_5A_POLYTECH**. Préparation mise à jour le 8 octobre 2026.

## Objectif actuel

Concevoir avec KiCad une carte électronique pour une mini-console : **écran LCD en haut, petits joysticks en bas**. La priorité est le schéma, les connexions, le placement, le routage et les fichiers de fabrication du PCB. L'intégration et le logiciel de jeu seront abordés ensuite selon le temps disponible et les attendus du professeur.

L'équipe dispose d'un écran, de joysticks et d'une carte STM32. Leurs références exactes restent à relever. Cette documentation est une **base de travail à compléter avec le binôme**, pas une conception validée.

## À ouvrir en premier

| Document | Usage |
|---|---|
| [Préparation de la séance](Documents/01-Planning-Budget/Preparation_09-10-2026.md) | Ordre de travail et premiers exercices KiCad |
| [Périmètre et fonctions](Documents/03-Specifications/Cadrage_mini_console.md) | Besoin, décisions et questions au professeur |
| [Architecture à compléter](Documents/02-Architecture-Diagrammes/MiniConsole_architecture.md) | Diagramme visible sur GitHub et fichier Draw.io éditable |
| [Composants et documentation](Datasheet/README.md) | Fiches à remplir et liens officiels ST |
| [Table de connexions](Documents/11-Pin-Out%20MCU/Connexions_a_completer.md) | Broches des modules, connecteurs et STM32 |
| [Bilan d'alimentation](Documents/13-Bilan%20Puissance%20etThermique/Power_budget_a_completer.md) | Tensions et courants à renseigner |

## Point d'architecture à trancher

Le template KiCad contient le symbole **STM32F446RETx** : il prévoit un microcontrôleur directement sur le PCB. Il faut confirmer avec le professeur si la carte STM32 disponible sert uniquement aux essais, ou si une carte porteuse accueillant cette carte complète est autorisée. Ces deux solutions n'ont ni les mêmes connecteurs ni le même schéma.

Même si l'écran et les joysticks sont montés plus tard, leurs tensions, brochages, dimensions et fixations doivent être connus avant de fabriquer la carte.

## État réel au 8 octobre 2026

- Idée et premier schéma bloc discutés ; références matérielles non confirmées.
- Projet KiCad et documents techniques hérités du template présents.
- Nouveau dossier de préparation ajouté ; les cases restent à compléter.
- Aucun pinout final, aucun circuit validé et aucun fichier prêt à fabriquer.
- Le guide prévoit un PCB **4 couches** ; le fichier PCB hérité est actuellement configuré en **2 couches**, à ajuster avant le routage.

## Les outils

- **KiCad** : schéma électrique, empreintes, placement, pistes et exports de fabrication.
- **STM32CubeMX** : sélection du STM32 et configuration de ses broches/périphériques.
- **Draw.io** : diagrammes fonctionnels et matériels.
- **GitHub** : partage des fichiers et historique des modifications.

Pour commencer dans KiCad, ouvrir `Projet_KICAD/Projet_PCBPolytech_git.kicad_pro`. Faire les exercices de découverte dans un projet séparé.

## Travail à deux sur GitHub

1. Récupérer la dernière version avant de travailler (pull).
2. Se répartir les fichiers ; éviter les modifications simultanées d'un même schéma ou PCB KiCad.
3. Enregistrer dans le logiciel, puis créer un commit avec un message clair.
4. Envoyer le commit sur GitHub (push) pour que le binôme puisse le récupérer.

Un commit est une étape enregistrée de l'historique. Une sauvegarde locale KiCad seule ne met pas GitHub à jour. Les fichiers `empty.md` sont des repères du template et peuvent rester tant que leur dossier est en cours de remplissage.
