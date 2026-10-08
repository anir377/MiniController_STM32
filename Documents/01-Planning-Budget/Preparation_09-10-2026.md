# Préparer la séance du vendredi 9 octobre 2026

**Horaire : 8h30–12h30.** D'après le mail du professeur, le schéma doit être bien avancé en fin de séance, surtout sur les parties communes et imposées. Les principaux choix d'architecture et de composants doivent être clarifiés.

## Ce soir : découverte ciblée de KiCad

Proposition de prise en main de 60 à 90 minutes, à adapter au temps disponible :

1. Ouvrir un projet et distinguer éditeur de schéma et éditeur de PCB.
2. Dans un projet d'exercice séparé, placer un connecteur, une résistance et une LED ; les relier.
3. Comprendre le **symbole** (représentation électrique) et l'**empreinte** (pastilles et dimensions physiques).
4. Affecter les empreintes, lancer le contrôle électrique ERC et lire les messages.
5. Transférer le schéma au PCB, tracer un contour, placer les composants et quelques pistes.
6. Découvrir le contrôle DRC et la vue 3D.

### Ressources

- [Tutoriel en français proposé dans le guide : Premier PCB avec KiCad 8, saisie de schéma](https://youtu.be/Aj7RpaX0Y7o). Prioritaire pour débuter ; certains menus diffèrent selon la version.
- [Documentation officielle française : Démarrer avec KiCad 9](https://docs.kicad.org/9.0/fr/getting_started_in_kicad/getting_started_in_kicad.html).
- [Phil's Lab #65 : conception STM32 sous KiCad](https://www.youtube.com/watch?v=aVUqaB0IMh4). Proposé par le guide ; à regarder ensuite. Son exemple utilise 2 couches, le projet du cours en demande 4.

KiCad sert à concevoir les circuits imprimés. QCAD est un outil de dessin technique 2D : il n'est pas nécessaire pour cette prise en main.

## Préparer le matériel et les choix

- [ ] Photographier recto et verso de l'écran, de chaque type de joystick et de la carte STM32.
- [ ] Relever les références et inscriptions des broches.
- [ ] Mesurer modules, pas des connecteurs et positions des trous de fixation.
- [ ] Confirmer le nombre de joysticks et de boutons.
- [ ] Décider avec le professeur : STM32 directement sur le PCB ou carte STM32 sur connecteurs ?
- [ ] Identifier les tensions d'alimentation et niveaux logiques des modules.
- [ ] Compléter le diagramme et le tableau des composants.

## Pendant la séance : ordre proposé

1. Faire valider le périmètre et les éléments communs imposés.
2. Identifier précisément le matériel disponible et récupérer ses documents.
3. Définir l'alimentation et les connecteurs.
4. Préparer le pinout dans STM32CubeMX, avec les broches de programmation et de test réservées.
5. Avancer le schéma KiCad autour du STM32, de l'alimentation et des interfaces des modules.
6. Relire avec le binôme, enregistrer les décisions et partager les fichiers sur GitHub.

## Avant de demander la fabrication, plus tard

- [ ] Schéma, brochage des connecteurs et empreintes vérifiés avec le matériel réel.
- [ ] Dimensions, fixations et dégagements mécaniques vérifiés.
- [ ] Configuration 4 couches et règles du fabricant appliquées.
- [ ] ERC et DRC examinés ; erreurs corrigées et exceptions justifiées.
- [ ] Gerber et fichiers de perçage exportés et inspectés.
- [ ] Si assemblage demandé : nomenclature (BOM) et fichier de positions des composants vérifiés.
- [ ] Validation du professeur obtenue selon les consignes du cours.

La fabrication du **PCB nu** produit la carte et ses pistes. L'**assemblage** ajoute les composants soudés : c'est une prestation distincte à préciser au fournisseur.
