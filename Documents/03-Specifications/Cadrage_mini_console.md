# Mini-console : cadrage provisoire

Date : 8 octobre 2026. Statut : proposition à compléter en binôme.

## Besoin

Concevoir un PCB destiné à une mini-console, avec écran LCD en haut et joysticks en bas. Le travail immédiat concerne la conception électronique et les fichiers nécessaires à la fabrication. Les modules sont disponibles, mais leur identification reste à faire.

## Fonctions et solutions envisagées

| Fonction | Solution envisagée | Décision restant à prendre |
|---|---|---|
| Recevoir les commandes | Joysticks et boutons | Nombre, référence, signaux analogiques ou numériques |
| Traiter les commandes et piloter l'affichage | STM32F4 | Référence et intégration directe ou carte porteuse |
| Affichage| Module LCD disponible | Référence, capacité graphique, interface et connecteur |
| Distribuer l'énergie | Entrée, protections et DC/DC du socle commun | Source, tensions, courant et références |
| Programmer et tester | SWD, UART, LED et bouton de test | Affectation des broches et connecteurs |
| Maintenir et relier les modules | PCB, connecteurs et fixations | Dimensions, empreintes et dégagements |

## Périmètre de la première version

Priorité : écran, commandes, STM32, alimentation, programmation/test et interfaces nécessaires. Batterie rechargeable, audio et microSD étaient présents dans le premier schéma bloc ; ils ne sont pas des choix validés et ne sont pas retenus d'office dans cette base. À décider : conservés, prévus en option ou retirés.

## Deux architectures possibles, à départager

| Variante | Contenu du PCB conçu | Conséquence |
|---|---|---|
| STM32 directement soudé | MCU, alimentation, circuits associés, interfaces et connecteurs des modules | Variante suggérée par le template ; concevoir aussi le support électrique du MCU |
| Carte porteuse | Connecteurs accueillant la carte STM32 existante et les modules | À faire autoriser ; vérifier brochage, encombrement et chemins d'alimentation de la carte complète |

Le symbole STM32F446RETx du template n'identifie pas à lui seul la carte effectivement remise à l'équipe. Ne pas reprendre un schéma Nucleo entier sans déterminer quelles fonctions seront réellement utilisées.

## Décisions à renseigner

| Sujet | Décision | Preuve / validation |
|---|---|---|
| Variante d'intégration STM32 | À confirmer | Professeur + référence de la carte |
| Référence LCD / interface | À confirmer | Photo + documentation du module |
| Nombre et référence des joysticks | À confirmer | Matériel réel |
| Dimensions finales | À confirmer | Contraintes du cours + mesures |
| Alimentation / connecteur | À confirmer | Bilan de puissance + validation |
| Nombre de couches | 4 selon le guide | Mettre à jour les réglages KiCad |
| Fabrication seule ou assemblage | À confirmer | Consignes + prestation fournisseur |

## Questions 

1. Le MCU doit-il obligatoirement être soudé sur notre PCB ?
2. Quels composants et interfaces communs faut-il impérativement intégrer ?
3. Les modules écran et joysticks seront-ils enfichés, reliés par câble ou soudés ?
4. Quelles limites exactes appliquer aux dimensions, au nombre de composants et à l'assemblage ?
5. Quels tests et livrables logiciels restent obligatoires après fabrication ?
